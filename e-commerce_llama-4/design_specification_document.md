**Technical Design Specification Document for The Scent E-Commerce Platform**
================================================================================

**Table of Contents**
-----------------

1. [Overview of Design Requirements](#overview-of-design-requirements)
2. [Design Methodology and Approach](#design-methodology-and-approach)
3. [System Architecture](#system-architecture)
4. [Database Design](#database-design)
5. [Backend Implementation (Laravel)](#backend-implementation-laravel)
6. [Frontend Implementation (Blade, CSS, JS)](#frontend-implementation-blade-css-js)
7. [Shopping Cart & Payment Gateway Integration](#shopping-cart--payment-gateway-integration)
8. [Security Considerations](#security-considerations)
9. [Testing Strategy](#testing-strategy)
10. [Deployment Strategy](#deployment-strategy)
11. [Monitoring and Maintenance](#monitoring-and-maintenance)
12. [Conclusion and Recommendations](#conclusion-and-recommendations)
13. **Appendix**:
    - [A: Step-by-Step Environment Setup Guide](#appendix-a-step-by-step-environment-setup-guide)
    - [B: Detailed Deployment Guide for The Scent Project](#appendix-b-detailed-deployment-guide-for-the-scent-project)
    - [C: Code Repository Structure](#appendix-c-code-repository-structure)

---

**Overview of Design Requirements**
----------------------------------

The Scent is an e-commerce platform designed to promote mental and physical well-being through aromatherapy products, including essential oils and natural soaps. The platform must:

1. **Provide a seamless user experience**:
   - Responsive design for mobile and desktop.
   - Interactive product catalog with filtering and search.
   - Quick View modal for product details.
2. **Enable secure transactions**:
   - Integrate Stripe for payment processing.
   - Implement CSRF protection and input validation.
3. **Support business operations**:
   - Admin panel for managing products, orders, and users.
   - Automated order status updates (e.g., "pending" to "shipped").
4. **Scale for growth**:
   - Optimized database schema for performance.
   - Caching mechanisms for frequently accessed data.
5. **Ensure reliability and availability**:
   - Deploy on Apache2 with SSL encryption.
   - Monitor server logs and application performance.

**Design Methodology and Approach**
-----------------------------------

The project follows a **modular, iterative development approach**:

1. **Requirements Gathering**:
   - Identified functional (user registration, cart, checkout) and non-functional (security, scalability) requirements.
2. **System Design**:
   - Designed database schema, system architecture, and component interactions.
3. **Implementation**:
   - Developed backend (Laravel) and frontend (Blade, CSS, JS) components.
   - Integrated third-party services (Stripe, Certbot for SSL).
4. **Testing & Validation**:
   - Unit tests, feature tests, and manual testing for critical flows.
5. **Deployment**:
   - Configured Apache2, optimized Laravel, and secured the server.

**System Architecture**
----------------------

The Scent platform is built as a **monolithic web application** with the following layers:

```plaintext
+------------------+      +------------------+      +------------------+
|     Client       | ---> |     Apache2      | ---> |  Laravel (PHP)   |
| (Browser, Mobile)|      |  (Web Server)    |      |  (Backend Logic) |
+------------------+      +------------------+      +------------------+
                                                           |
                                                           |
                                                           v
                                                 +------------------+
                                                 |     MySQL        |
                                                 |  (Relational DB) |
                                                 +------------------+
                                                           |
                                                           |
                                                           v
                                                 +------------------+
                                                 |    Stripe API    |
                                                 | (Payment Gateway)|
                                                 +------------------+
```

**Key Components**:
- **Apache2**: Handles HTTP/HTTPS requests, routes them to Laravel's `public/index.php`.
- **Laravel**: Manages routing, authentication, business logic, and database interactions.
- **MySQL**: Stores users, products, orders, and reviews.
- **Stripe**: Processes payments securely via Laravel Cashier.

**Database Design**
-------------------

The relational database schema is optimized for e-commerce operations:

```sql
CREATE TABLE users (
    id BIGINT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(255),
    email VARCHAR(255) UNIQUE,
    password VARCHAR(255),
    role ENUM('customer', 'admin') DEFAULT 'customer',
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

CREATE TABLE products (
    id BIGINT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(255),
    description TEXT,
    price DECIMAL(10, 2),
    stock INT,
    category ENUM('essential_oil', 'soap'),
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

CREATE TABLE orders (
    id BIGINT PRIMARY KEY AUTO_INCREMENT,
    user_id BIGINT,
    total_amount DECIMAL(10, 2),
    status ENUM('pending', 'shipped', 'delivered'),
    FOREIGN KEY (user_id) REFERENCES users(id) ON DELETE CASCADE,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

CREATE TABLE order_items (
    id BIGINT PRIMARY KEY AUTO_INCREMENT,
    order_id BIGINT,
    product_id BIGINT,
    quantity INT,
    FOREIGN KEY (order_id) REFERENCES orders(id) ON DELETE CASCADE,
    FOREIGN KEY (product_id) REFERENCES products(id) ON DELETE CASCADE
);

CREATE TABLE reviews (
    id BIGINT PRIMARY KEY AUTO_INCREMENT,
    user_id BIGINT,
    product_id BIGINT,
    rating TINYINT,
    comment TEXT,
    FOREIGN KEY (user_id) REFERENCES users(id) ON DELETE CASCADE,
    FOREIGN KEY (product_id) REFERENCES products(id) ON DELETE CASCADE
);
```

**Rationale**:
- **ENUM for `category` and `status`**: Reduces storage overhead and ensures data consistency.
- **Foreign Keys**: Maintains referential integrity (e.g., deleting a user cascades to their orders).
- **Timestamps**: Tracks creation and update times for auditing.

**Backend Implementation (Laravel)**
--------------------------------------

Laravel powers the backend with **MVC (Model-View-Controller) architecture**:

### **Models (Eloquent ORM)**

```php
// app/Models/Product.php
namespace App\Models;

use Illuminate\Database\Eloquent\Model;
use Illuminate\Database\Eloquent\Relations\HasMany;

class Product extends Model {
    protected $fillable = ['name', 'description', 'price', 'stock', 'category'];

    public function reviews(): HasMany {
        return $this->hasMany(Review::class);
    }
}
```

### **Controllers**

```php
// app/Http/Controllers/ProductController.php
namespace App\Http\Controllers;

use App\Models\Product;
use Illuminate\Http\Request;

class ProductController extends Controller {
    public function index() {
        $products = Product::all();
        return view('products.index', compact('products'));
    }

    public function store(Request $request) {
        $validated = $request->validate([
            'name' => 'required',
            'price' => 'required|numeric',
        ]);
        Product::create($validated);
        return redirect()->route('products.index')->with('success', 'Product added!');
    }
}
```

### **Routes (web.php)**

```php
Route::get('/products', [ProductController::class, 'index'])->name('products.index');
Route::post('/products', [ProductController::class, 'store'])->middleware('admin');
```

**Middleware for Admin Access**:

```php
// app/Http/Middleware/AdminMiddleware.php
public function handle(Request $request, Closure $next) {
    if (Auth::user()->role !== 'admin') {
        abort(403, 'Unauthorized');
    }
    return $next($request);
}
```

**Frontend Implementation (Blade, CSS, JS)**
---------------------------------------------

### **Blade Templates**

**`resources/views/products/index.blade.php`**:

```blade
@extends('layouts.app')

@section('content')
    <h1>Our Products</h1>
    <div class="product-grid">
        @foreach($products as $product)
            <div class="product-card">
                <img src="{{ $product->image }}" alt="{{ $product->name }}">
                <h3>{{ $product->name }}</h3>
                <p>${{ $product->price }}</p>
                <form action="{{ route('cart.add', $product->id) }}" method="POST">
                    @csrf
                    <button type="submit">Add to Cart</button>
                </form>
            </div>
        @endforeach
    </div>
@endsection
```

### **CSS (SASS/SCSS Optional)**

**`public/css/app.css`**:

```css
.product-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
}

.product-card {
    background: #fff;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.product-card img {
    width: 100%;
    height: 200px;
    object-fit: cover;
    border-radius: 10px 10px 0 0;
}
```

### **JavaScript (AJAX for Cart)**

**`public/js/cart.js`**:

```javascript
document.querySelectorAll('.add-to-cart').forEach(button => {
    button.addEventListener('click', async (e) => {
        e.preventDefault();
        const productId = button.dataset.id;
        await fetch(`/cart/add/${productId}`, { method: 'POST', headers: { 'X-CSRF-TOKEN': csrfToken } });
        alert('Product added to cart!');
    });
});
```

**Shopping Cart & Payment Gateway Integration**
-----------------------------------------------

### **Cart Logic (bumbummen99/shoppingcart)**

**`app/Http/Controllers/CartController.php`**:

```php
use Gloudemans\Shoppingcart\Facades\Cart;

class CartController extends Controller {
    public function add($id) {
        $product = Product::find($
