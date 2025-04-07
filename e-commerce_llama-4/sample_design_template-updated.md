Okay, I have carefully reviewed all the provided documents (`design_specification_document_2.md`, `design_specification_document.md`, `deploy_guide.md`, `sample_design_template.md`) and the company description for "The Scent".

My goal is to synthesize the best aspects of these documents, resolve inconsistencies, incorporate the company's identity and product focus, and produce a single, comprehensive, and updated Technical Design Specification Document using the Apache2 + PHP (Laravel) + MySQL stack. I will use the structure from `design_specification_document_2.md` as a base due to its clarity and modernity, integrating relevant details and refinements from the other documents and the prompt.

Here is the consolidated and improved Technical Design Specification Document:

---

# Technical Design Specification Document
## The Scent E-commerce Platform

**Version:** 2.0
**Date:** 2024-05-16
**Author:** AI System Architect (Synthesized from provided documents)

## Table of Contents

1.  [Executive Summary](#1-executive-summary)
2.  [Project Overview](#2-project-overview)
    *   [2.1 Company Background & Mission](#21-company-background--mission)
    *   [2.2 Business Requirements](#22-business-requirements)
    *   [2.3 Functional Requirements](#23-functional-requirements)
    *   [2.4 Non-Functional Requirements](#24-non-functional-requirements)
    *   [2.5 Design Goals](#25-design-goals)
3.  [System Architecture](#3-system-architecture)
    *   [3.1 High-Level Architecture](#31-high-level-architecture)
    *   [3.2 Technology Stack](#32-technology-stack)
    *   [3.3 Key Components](#33-key-components)
    *   [3.4 Implementation Approach (MVC)](#34-implementation-approach-mvc)
4.  [Database Design](#4-database-design)
    *   [4.1 Schema Overview](#41-schema-overview)
    *   [4.2 Table Definitions & Rationale](#42-table-definitions--rationale)
    *   [4.3 Relationships](#43-relationships)
5.  [Backend Implementation (Laravel 10)](#5-backend-implementation-laravel-10)
    *   [5.1 Core Framework Setup](#51-core-framework-setup)
    *   [5.2 Models (Eloquent ORM)](#52-models-eloquent-orm)
    *   [5.3 Controllers](#53-controllers)
    *   [5.4 Routes (web.php)](#54-routes-webphp)
    *   [5.5 Middleware](#55-middleware)
    *   [5.6 Service Classes](#56-service-classes)
    *   [5.7 Shopping Cart Logic](#57-shopping-cart-logic)
    *   [5.8 Payment Gateway Integration (Stripe)](#58-payment-gateway-integration-stripe)
6.  [Frontend Implementation (Blade, CSS, JS)](#6-frontend-implementation-blade-css-js)
    *   [6.1 Templating Engine (Blade)](#61-templating-engine-blade)
    *   [6.2 Styling (CSS/SCSS)](#62-styling-cssscss)
    *   [6.3 Interactivity (JavaScript ES6+)](#63-interactivity-javascript-es6)
    *   [6.4 Key UI Components & "Wow Effect"](#64-key-ui-components--wow-effect)
    *   [6.5 Responsive Design](#65-responsive-design)
7.  [Security Measures](#7-security-measures)
    *   [7.1 Authentication & Authorization](#71-authentication--authorization)
    *   [7.2 Data Validation & Sanitization](#72-data-validation--sanitization)
    *   [7.3 CSRF Protection](#73-csrf-protection)
    *   [7.4 XSS Prevention](#74-xss-prevention)
    *   [7.5 SQL Injection Prevention](#75-sql-injection-prevention)
    *   [7.6 Password Hashing](#76-password-hashing)
    *   [7.7 HTTPS/SSL Encryption](#77-httpsssl-encryption)
    *   [7.8 Server & File Permissions](#78-server--file-permissions)
8.  [Testing Strategy](#8-testing-strategy)
    *   [8.1 Unit Testing](#81-unit-testing)
    *   [8.2 Feature Testing](#82-feature-testing)
    *   [8.3 Manual Testing](#83-manual-testing)
    *   [8.4 Tools](#84-tools)
9.  [Deployment Strategy](#9-deployment-strategy)
    *   [9.1 Environment Setup (LAMP Stack)](#91-environment-setup-lamp-stack)
    *   [9.2 Deployment Process](#92-deployment-process)
    *   [9.3 Server Configuration (Apache2)](#93-server-configuration-apache2)
    *   [9.4 Post-Deployment Verification](#94-post-deployment-verification)
10. [Performance Optimization](#10-performance-optimization)
    *   [10.1 Caching Strategy (Redis)](#101-caching-strategy-redis)
    *   [10.2 Database Optimization](#102-database-optimization)
    *   [10.3 Frontend Optimization](#103-frontend-optimization)
    *   [10.4 Server-Side Optimization](#104-server-side-optimization)
11. [Monitoring and Maintenance](#11-monitoring-and-maintenance)
    *   [11.1 Logging](#111-logging)
    *   [11.2 Monitoring Tools](#112-monitoring-tools)
    *   [11.3 Backup Strategy](#113-backup-strategy)
    *   [11.4 Scheduled Tasks (Cron)](#114-scheduled-tasks-cron)
12. [Conclusions and Recommendations](#12-conclusions-and-recommendations)
    *   [12.1 Summary](#121-summary)
    *   [12.2 Future Enhancements](#122-future-enhancements)
13. [Appendix A: Detailed Deployment Guide](#appendix-a-detailed-deployment-guide)
14. [Appendix B: Code Repository Structure](#appendix-b-code-repository-structure)
15. [Appendix C: Performance Optimization Checklist](#appendix-c-performance-optimization-checklist)

---

## 1. Executive Summary

The Scent E-commerce Platform is designed as a sophisticated online retail system focused on promoting mental and physical well-being through high-quality aromatherapy products, specifically essential oils and natural soaps. Leveraging globally sourced raw materials and unique formulations, the platform aims to provide a seamless, secure, and engaging user experience. This document outlines the technical design, architecture, and implementation strategy using a modern LAMP stack (Apache2, MySQL 8.0, PHP 8.2 with Laravel 10), incorporating best practices for security, scalability, and performance.

## 2. Project Overview

### 2.1 Company Background & Mission

*The Scent* produces a range of aromatherapy products, importing high-quality raw materials globally and exporting finished goods crafted with unique formulations. The company emphasizes the relevance of aromatherapy in managing modern stress and aims to create harmonious, balanced products that promote mental and physical health.

### 2.2 Business Requirements

The platform must support:
*   Showcasing and selling essential oils and natural soaps.
*   Secure online transactions.
*   Efficient management of products, orders, and customers.
*   A brand image reflecting quality, natural ingredients, and well-being.

### 2.3 Functional Requirements

*   **Customer Facing:**
    *   User Registration & Login (including social login options - Future)
    *   Product Catalog Browsing (with images, descriptions)
    *   Advanced Product Filtering (by category, price, rating) & Search
    *   Detailed Product View (including multiple images, potentially 3D view/video)
    *   Product Reviews & Ratings System
    *   Shopping Cart Management (Add, Update, Remove items)
    *   Secure Checkout Process (Stripe integration)
    *   Order History & Tracking
    *   User Profile Management
    *   Responsive Design (Desktop, Tablet, Mobile)
*   **Administrator Facing (Admin Panel):**
    *   Secure Admin Login
    *   Dashboard with Key Metrics (Sales, Orders, Users)
    *   Product Management (CRUD operations for products, categories, inventory)
    *   Order Management (View orders, Update status: pending, processing, shipped, delivered, cancelled)
    *   Customer Management (View users, Manage roles)
    *   Review Management (Approve, Delete reviews)
    *   Content Management (Manage static pages, potentially blog posts - Future)

### 2.4 Non-Functional Requirements

*   **Security:** Robust protection against common web vulnerabilities (CSRF, XSS, SQLi), secure payment processing (PCI-DSS compliance via Stripe), HTTPS encryption.
*   **Performance:** Fast page load times, efficient database queries, optimized assets, effective caching. Target TTFB < 500ms, LCP < 2.5s.
*   **Scalability:** Architecture should handle increasing traffic and product catalog size. Horizontal scaling potential for web servers and database read replicas.
*   **Reliability:** High availability (target 99.9% uptime), robust error handling, regular backups.
*   **Maintainability:** Clean, well-documented code following PSR standards and Laravel best practices. Modular design.
*   **Usability:** Intuitive navigation, clear CTAs, accessible design (WCAG AA compliance - Future Goal).

### 2.5 Design Goals

*   **User Experience:** Create a visually appealing, calming, and trustworthy interface reflecting The Scent's brand identity. Incorporate interactive elements ("Wow Effect") like subtle animations (AOS), potentially 3D product views, and features like Quick View modals to enhance engagement.
*   **Modularity:** Build reusable components and services for easier maintenance and future expansion.
*   **Security-First:** Integrate security considerations throughout the design and development process.
*   **Performance-Oriented:** Optimize from the start using efficient code, database indexing, and caching.

## 3. System Architecture

### 3.1 High-Level Architecture

The platform utilizes a monolithic application architecture based on the Model-View-Controller (MVC) pattern, deployed on a standard LAMP stack with enhancements for performance.

```plaintext
+------------------+      +---------------------+      +------------------+      +----------------+
|  Client Browser  | <--> |    Apache2 Server   | ---> | Laravel (PHP 8.2)| <--> | MySQL 8.0 DB   |
| (Desktop/Mobile) |      | (HTTPS, mod_rewrite)|      | (MVC, Eloquent)  |      | (InnoDB Engine)|
+------------------+      +---------------------+      +------------------+      +----------------+
                                 ^         ^                    |                      ^
                                 |         |                    |                      |
                                 |         +--------------------v----------------------+
                                 |                    +------------------+
                                 |                    |   Redis Cache    |
                                 |                    | (Sessions, Query)|
                                 |                    +------------------+
                                 |
                                 +--------------------v------------------+
                                                    |    Stripe API    |
                                                    | (Payment Gateway)|
                                                    +------------------+
```

### 3.2 Technology Stack

*   **Web Server:** Apache 2.4 (with `mod_rewrite`, `mod_ssl`, `mod_deflate`, `mod_headers`)
*   **Backend:** PHP 8.2
*   **Framework:** Laravel 10
*   **Database:** MySQL 8.0 (InnoDB Engine)
*   **Frontend:** HTML5, CSS3 (potentially SCSS), JavaScript (ES6+)
*   **Templating:** Laravel Blade
*   **Caching:** Redis (for sessions, application cache, queue - Future)
*   **Payment Gateway:** Stripe (via Laravel Cashier or direct SDK)
*   **Package Management:** Composer (PHP), NPM (JS)
*   **Version Control:** Git

### 3.3 Key Components

1.  **Web Server (Apache2):** Handles incoming HTTP/S requests, serves static assets, and forwards dynamic requests to the Laravel application via `public/index.php`. Manages SSL termination.
2.  **Application Layer (Laravel):** Contains the core business logic, routing, data handling (Eloquent ORM), templating (Blade), authentication, session management, and integration with third-party services (Stripe, Redis).
3.  **Database Layer (MySQL):** Persists application data including users, products, orders, reviews, etc. Uses InnoDB for ACID compliance and foreign key support.
4.  **Caching Layer (Redis):** Provides fast, in-memory storage for frequently accessed data (e.g., configuration, routes, sessions, expensive query results) to reduce database load and improve response times.
5.  **Payment Gateway (Stripe):** Securely handles credit card processing off-site, reducing PCI compliance scope for the application.

### 3.4 Implementation Approach (MVC)

The Laravel framework enforces the MVC pattern:
*   **Models (`app/Models/`):** Represent database tables (e.g., `Product`, `User`, `Order`) and handle data interaction logic using Eloquent ORM.
*   **Views (`resources/views/`):** Define the presentation layer using Blade templates. They receive data from controllers and render the HTML output.
*   **Controllers (`app/Http/Controllers/`):** Handle user requests, interact with models to fetch or manipulate data, and pass data to views for rendering. Contain the primary application logic.

**Project Directory Structure (Simplified):**

```plaintext
the-scent/
├── app/
│   ├── Console/         # Artisan commands
│   ├── Exceptions/      # Exception handling
│   ├── Http/
│   │   ├── Controllers/ # Request handling logic
│   │   ├── Middleware/  # Request filtering (Auth, Admin, CSRF)
│   │   └── Requests/    # Form Request Validation
│   ├── Models/          # Eloquent Models
│   ├── Providers/       # Service Providers
│   └── Services/        # Business logic services (Optional)
├── bootstrap/           # Framework bootstrapping
├── config/              # Application configuration files
├── database/
│   ├── factories/       # Model factories for testing/seeding
│   ├── migrations/      # Database schema definitions
│   └── seeders/         # Database seeding
├── public/              # Web server document root
│   ├── css/
│   ├── js/
│   ├── images/          # Product images, assets
│   └── index.php        # Application entry point
├── resources/
│   ├── css/             # Raw SCSS/CSS files (if using build process)
│   ├── js/              # Raw JS files (if using build process)
│   ├── lang/            # Language files
│   └── views/           # Blade templates
├── routes/              # Route definitions (web.php, api.php)
├── storage/             # Compiled views, sessions, logs, user uploads
├── tests/               # Unit and Feature tests
├── vendor/              # Composer dependencies
├── .env                 # Environment configuration
├── artisan              # Laravel command-line interface
├── composer.json        # PHP dependencies
└── package.json         # JS dependencies (for build process)
```
*(Reference Appendix B for a more detailed structure)*

## 4. Database Design

### 4.1 Schema Overview

A relational database schema using MySQL 8.0 with the InnoDB engine will be employed. The design emphasizes normalization to reduce data redundancy while using appropriate indexing for performance. Foreign keys ensure referential integrity.

### 4.2 Table Definitions & Rationale

```sql
-- Users Table: Stores customer and administrator accounts
CREATE TABLE users (
    id BIGINT UNSIGNED AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(255) NOT NULL,
    email VARCHAR(255) NOT NULL UNIQUE,
    email_verified_at TIMESTAMP NULL,
    password VARCHAR(255) NOT NULL,
    remember_token VARCHAR(100) NULL,
    role ENUM('customer', 'admin') NOT NULL DEFAULT 'customer',
    created_at TIMESTAMP NULL DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;

-- Products Table: Stores details about essential oils and soaps
CREATE TABLE products (
    id BIGINT UNSIGNED AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(255) NOT NULL,
    slug VARCHAR(255) NOT NULL UNIQUE, -- For SEO-friendly URLs
    description TEXT NULL,
    image_url VARCHAR(255) NULL, -- Primary image URL
    price DECIMAL(10, 2) NOT NULL,
    stock INT UNSIGNED NOT NULL DEFAULT 0,
    category ENUM('essential_oil', 'soap') NOT NULL,
    is_featured BOOLEAN NOT NULL DEFAULT FALSE, -- To highlight specific products
    created_at TIMESTAMP NULL DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
    INDEX idx_category (category),
    INDEX idx_is_featured (is_featured),
    FULLTEXT idx_fulltext_name_desc (name, description) -- For full-text search
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;

-- Orders Table: Stores high-level order information
CREATE TABLE orders (
    id BIGINT UNSIGNED AUTO_INCREMENT PRIMARY KEY,
    user_id BIGINT UNSIGNED NOT NULL,
    order_number VARCHAR(50) NOT NULL UNIQUE, -- User-friendly order identifier
    total_amount DECIMAL(10, 2) NOT NULL,
    status ENUM('pending', 'processing', 'shipped', 'delivered', 'cancelled') NOT NULL DEFAULT 'pending',
    stripe_payment_id VARCHAR(255) NULL, -- Reference to Stripe payment
    shipping_address TEXT NULL, -- Store serialized address or use separate address table
    billing_address TEXT NULL, -- Store serialized address or use separate address table
    created_at TIMESTAMP NULL DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
    FOREIGN KEY (user_id) REFERENCES users(id) ON DELETE RESTRICT, -- Prevent user deletion if orders exist
    INDEX idx_status (status),
    INDEX idx_created_at (created_at)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;

-- Order Items Table: Links products to orders (Many-to-Many relationship)
CREATE TABLE order_items (
    id BIGINT UNSIGNED AUTO_INCREMENT PRIMARY KEY,
    order_id BIGINT UNSIGNED NOT NULL,
    product_id BIGINT UNSIGNED NOT NULL,
    quantity INT UNSIGNED NOT NULL,
    price_at_purchase DECIMAL(10, 2) NOT NULL, -- Price when the order was placed
    created_at TIMESTAMP NULL DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
    FOREIGN KEY (order_id) REFERENCES orders(id) ON DELETE CASCADE, -- If order is deleted, items are deleted
    FOREIGN KEY (product_id) REFERENCES products(id) ON DELETE RESTRICT -- Prevent product deletion if used in orders
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;

-- Reviews Table: Stores customer reviews for products
CREATE TABLE reviews (
    id BIGINT UNSIGNED AUTO_INCREMENT PRIMARY KEY,
    user_id BIGINT UNSIGNED NOT NULL,
    product_id BIGINT UNSIGNED NOT NULL,
    rating TINYINT UNSIGNED NOT NULL CHECK (rating >= 1 AND rating <= 5),
    comment TEXT NULL,
    is_approved BOOLEAN NOT NULL DEFAULT FALSE, -- Admin moderation
    created_at TIMESTAMP NULL DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
    FOREIGN KEY (user_id) REFERENCES users(id) ON DELETE CASCADE,
    FOREIGN KEY (product_id) REFERENCES products(id) ON DELETE CASCADE,
    INDEX idx_product_rating (product_id, rating),
    INDEX idx_approved_product (is_approved, product_id)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;

-- Optional: Categories Table (If more complex categories needed later)
-- Optional: Addresses Table (For reusable user addresses)
-- Optional: Product Images Table (For multiple images per product)

```

**Rationale**:
*   **`ENUM`**: Used for predefined, limited sets like `role`, `category`, `status` for data integrity and efficiency. Snake_case used for consistency.
*   **`UNSIGNED`**: Used for IDs and stock where values cannot be negative.
*   **`Timestamps`**: Laravel's standard `created_at` and `updated_at` are used.
*   **`Foreign Keys`**: Enforce relationships. `ON DELETE RESTRICT` is used cautiously to prevent accidental data loss (e.g., deleting a user with orders), while `ON DELETE CASCADE` is used where logical (e.g., deleting an order removes its items).
*   **`Indexes`**: Added on foreign keys, common filter columns (`category`, `status`, `is_featured`, `is_approved`), and for full-text search (`name`, `description` on `products`).
*   **`UNIQUE` Constraints**: Enforce uniqueness for `email`, `slug`, `order_number`.
*   **`Character Set/Collation`**: `utf8mb4` supports a wide range of characters, including emojis.

### 4.3 Relationships

Eloquent ORM will define these relationships in the Model classes:

*   **User:** `hasMany(Order)`, `hasMany(Review)`
*   **Product:** `hasMany(OrderItem)`, `hasMany(Review)`
*   **Order:** `belongsTo(User)`, `hasMany(OrderItem)`
*   **OrderItem:** `belongsTo(Order)`, `belongsTo(Product)`
*   **Review:** `belongsTo(User)`, `belongsTo(Product)`

```php
// Example: app/Models/Order.php
namespace App\Models;

use Illuminate\Database\Eloquent\Factories\HasFactory;
use Illuminate\Database\Eloquent\Model;
use Illuminate\Database\Eloquent\Relations\BelongsTo;
use Illuminate\Database\Eloquent\Relations\HasMany;

class Order extends Model
{
    use HasFactory;

    protected $fillable = [
        'user_id', 'order_number', 'total_amount', 'status',
        'stripe_payment_id', 'shipping_address', 'billing_address',
    ];

    public function user(): BelongsTo
    {
        return $this->belongsTo(User::class);
    }

    public function items(): HasMany // Renamed from orderItems for clarity
    {
        return $this->hasMany(OrderItem::class);
    }
}
```

## 5. Backend Implementation (Laravel 10)

### 5.1 Core Framework Setup

*   Install Laravel 10 via Composer.
*   Configure `.env` file (App Key, Database credentials, Cache driver, Session driver, Mail driver, Stripe keys).
*   Set up basic authentication using Laravel Breeze or Jetstream.

### 5.2 Models (Eloquent ORM)

*   Define models for each database table (`User`, `Product`, `Order`, `OrderItem`, `Review`).
*   Implement relationships (`hasMany`, `belongsTo`, etc.) as defined in [Section 4.3](#43-relationships).
*   Use `$fillable` or `$guarded` properties for mass assignment protection.
*   Utilize model factories for seeding and testing.

```php
// Example: app/Models/Product.php
namespace App\Models;

use Illuminate\Database\Eloquent\Factories\HasFactory;
use Illuminate\Database\Eloquent\Model;
use Illuminate\Database\Eloquent\Relations\HasMany;

class Product extends Model
{
    use HasFactory;

    protected $fillable = [
        'name', 'slug', 'description', 'image_url', 'price',
        'stock', 'category', 'is_featured',
    ];

    public function reviews(): HasMany
    {
        return $this->hasMany(Review::class);
    }

    public function orderItems(): HasMany
    {
        return $this->hasMany(OrderItem::class);
    }

    // Accessor for average rating (example)
    public function getAverageRatingAttribute(): ?float
    {
        return $this->reviews()->where('is_approved', true)->avg('rating');
    }

    // Add other necessary relationships or accessors/mutators
}
```

### 5.3 Controllers

*   Implement controllers for handling HTTP requests related to major resources (e.g., `ProductController`, `CartController`, `CheckoutController`, `OrderController`, `UserController`, `Admin/ProductController`, `Admin/OrderController`).
*   Follow Single Responsibility Principle where feasible.
*   Use dependency injection for services or repositories.
*   Employ Form Request Validation (`app/Http/Requests/`) for validating incoming data.

```php
// Example: app/Http/Controllers/ProductController.php
namespace App\Http\Controllers;

use App\Models\Product;
use Illuminate\Http\Request;
use Illuminate\View\View;

class ProductController extends Controller
{
    // Display a listing of the products (Catalog page)
    public function index(Request $request): View
    {
        $query = Product::query()->where('stock', '>', 0); // Only show in-stock items

        // Example Filtering
        if ($request->has('category')) {
            $query->where('category', $request->input('category'));
        }
        // Add sorting, pagination, search logic here

        $products = $query->paginate(12); // Paginate results
        return view('products.index', compact('products'));
    }

    // Display the specified product (Product Detail Page)
    public function show(Product $product): View // Route Model Binding
    {
         // Eager load approved reviews with user info
        $product->load(['reviews' => function ($query) {
            $query->where('is_approved', true)->with('user:id,name')->latest();
        }]);
        return view('products.show', compact('product'));
    }
}
```

### 5.4 Routes (web.php)

*   Define routes in `routes/web.php` for web interface and `routes/api.php` for potential future API needs.
*   Use route groups for organization (e.g., middleware groups for `auth`, `admin`).
*   Utilize resource controllers for standard CRUD operations.
*   Employ named routes for easy URL generation in views and redirects.

```php
// Example: routes/web.php
use App\Http\Controllers\ProfileController;
use App\Http\Controllers\ProductController;
use App\Http\Controllers\CartController;
use App\Http\Controllers\CheckoutController;
use App\Http\Controllers\Admin; // Namespace for Admin controllers
use Illuminate\Support\Facades\Route;

// Public Routes
Route::get('/', [ProductController::class, 'index'])->name('home'); // Or a dedicated HomeController
Route::get('/products', [ProductController::class, 'index'])->name('products.index');
Route::get('/products/{product:slug}', [ProductController::class, 'show'])->name('products.show'); // Use slug

// Cart Routes
Route::get('/cart', [CartController::class, 'index'])->name('cart.index');
Route::post('/cart/add/{product}', [CartController::class, 'add'])->name('cart.add');
Route::patch('/cart/update/{rowId}', [CartController::class, 'update'])->name('cart.update');
Route::delete('/cart/remove/{rowId}', [CartController::class, 'remove'])->name('cart.remove');

// Authenticated User Routes
Route::middleware('auth')->group(function () {
    // Profile (from Breeze/Jetstream)
    Route::get('/profile', [ProfileController::class, 'edit'])->name('profile.edit');
    Route::patch('/profile', [ProfileController::class, 'update'])->name('profile.update');
    Route::delete('/profile', [ProfileController::class, 'destroy'])->name('profile.destroy');

    // Checkout Process
    Route::get('/checkout', [CheckoutController::class, 'index'])->name('checkout.index'); // Show checkout form
    Route::post('/checkout', [CheckoutController::class, 'process'])->name('checkout.process'); // Handle submission
    Route::get('/checkout/success', [CheckoutController::class, 'success'])->name('checkout.success');
    Route::get('/checkout/cancel', [CheckoutController::class, 'cancel'])->name('checkout.cancel');

    // Order History
    // Route::get('/orders', [OrderController::class, 'index'])->name('orders.index');
    // Route::get('/orders/{order}', [OrderController::class, 'show'])->name('orders.show');

    // Reviews
    // Route::post('/products/{product}/reviews', [ReviewController::class, 'store'])->name('reviews.store');
});

// Admin Routes
Route::middleware(['auth', 'admin'])->prefix('admin')->name('admin.')->group(function () {
    Route::get('/dashboard', [Admin\DashboardController::class, 'index'])->name('dashboard');
    Route::resource('products', Admin\ProductController::class);
    Route::resource('orders', Admin\OrderController::class)->only(['index', 'show', 'update']); // Limit actions
    // Add routes for user management, review management etc.
});

// Auth Routes (Generated by Breeze/Jetstream)
require __DIR__.'/auth.php';

```

### 5.5 Middleware

*   Utilize built-in middleware: `auth` (authentication), `guest` (redirect if authenticated), `throttle` (rate limiting).
*   Create custom middleware:
    *   `AdminMiddleware`: Check if the authenticated user has the 'admin' role. Applied to admin routes.
    *   `EnsureEmailIsVerified`: (Optional, provided by Laravel) Ensure user's email is verified for certain actions.

```php
// Example: app/Http/Middleware/AdminMiddleware.php
namespace App\Http\Middleware;

use Closure;
use Illuminate\Http\Request;
use Illuminate\Support\Facades\Auth;
use Symfony\Component\HttpFoundation\Response;

class AdminMiddleware
{
    public function handle(Request $request, Closure $next): Response
    {
        if (!Auth::check() || Auth::user()->role !== 'admin') {
             // Redirect non-admins or unauthenticated users
            return redirect('/')->with('error', 'Access Denied. Administrator privileges required.');
           // Or abort(403, 'Unauthorized action.');
        }
        return $next($request);
    }
}
```
*(Register this in `app/Http/Kernel.php` under `$routeMiddleware`)*

### 5.6 Service Classes

*   For complex business logic not fitting neatly into models or controllers (e.g., complex order processing, inventory updates across multiple models), create dedicated service classes in `app/Services/`.
*   Inject these services into controllers via the service container.

```php
// Example: app/Services/InventoryService.php
namespace App\Services;

use App\Models\Product;
use App\Models\Order;
use Illuminate\Support\Facades\DB;
use App\Exceptions\InsufficientStockException;

class InventoryService
{
    // Decrease stock for products in an order
    public function decreaseStock(Order $order): void
    {
        DB::transaction(function () use ($order) {
            foreach ($order->items as $item) {
                $product = Product::findOrFail($item->product_id);
                if ($product->stock < $item->quantity) {
                    throw new InsufficientStockException("Insufficient stock for product: {$product->name}");
                }
                $product->decrement('stock', $item->quantity);
            }
        });
    }

    // Increase stock (e.g., for cancelled orders - more complex logic needed for returns)
    public function increaseStock(Order $order): void
    {
         DB::transaction(function () use ($order) {
            foreach ($order->items as $item) {
                Product::where('id', $item->product_id)->increment('stock', $item->quantity);
            }
        });
    }
}
```

### 5.7 Shopping Cart Logic

*   Utilize the `bumbummen99/shoppingcart` package (as detailed in `design_specification_document.md`) for session-based cart management.
*   Implement `CartController` methods for adding, updating, removing items, and displaying the cart.
*   Handle potential stock issues when adding items to the cart or during checkout.

```php
// Example: app/Http/Controllers/CartController.php (Using bumbummen99/shoppingcart)
namespace App\Http\Controllers;

use Gloudemans\Shoppingcart\Facades\Cart;
use App\Models\Product;
use Illuminate\Http\Request;
use Illuminate\Http\RedirectResponse;
use Illuminate\View\View;

class CartController extends Controller
{
    // Add item to cart
    public function add(Product $product): RedirectResponse // Route Model Binding
    {
        // Optional: Check stock before adding
        if ($product->stock < 1) {
            return back()->with('error', 'Sorry, this product is out of stock.');
        }

        Cart::add([
            'id'      => $product->id,
            'name'    => $product->name,
            'qty'     => 1, // Add validation for quantity input if provided
            'price'   => $product->price,
            'weight'  => 0, // Adjust if needed
            'options' => ['image_url' => $product->image_url, 'slug' => $product->slug]
        ]);

        return redirect()->route('cart.index')->with('success', "{$product->name} added to cart!");
    }

    // Display cart contents
    public function index(): View
    {
        return view('cart.index'); // Package provides Cart facade/helpers for view
    }

    // Update item quantity
    public function update(Request $request, $rowId): RedirectResponse
    {
        // Add validation for quantity
        $request->validate(['quantity' => 'required|integer|min:1']);

        // Optional: Check stock availability for the new quantity
        $item = Cart::get($rowId);
        $product = Product::find($item->id);
        if ($product && $product->stock < $request->quantity) {
             return back()->with('error', "Insufficient stock for {$product->name}. Only {$product->stock} available.");
        }

        Cart::update($rowId, $request->quantity);
        return redirect()->route('cart.index')->with('success', 'Cart updated.');
    }

    // Remove item from cart
    public function remove($rowId): RedirectResponse
    {
        Cart::remove($rowId);
        return redirect()->route('cart.index')->with('success', 'Item removed from cart.');
    }
}
```

### 5.8 Payment Gateway Integration (Stripe)

*   Use Laravel Cashier or Stripe's PHP SDK directly for processing payments.
*   Implement Stripe Checkout for a secure, hosted payment page (recommended for simplifying PCI compliance).
*   Handle payment success and failure callbacks/webhooks from Stripe.
*   On successful payment:
    *   Create the `Order` and `OrderItem` records.
    *   Decrease product stock (using `InventoryService`).
    *   Clear the shopping cart.
    *   Send order confirmation email.
    *   Redirect user to a success page.
*   On payment failure:
    *   Redirect user to a failure/retry page with appropriate messaging.
    *   Log the error.

```php
// Example: app/Http/Controllers/CheckoutController.php (using Stripe Checkout)
namespace App\Http\Controllers;

use Gloudemans\Shoppingcart\Facades\Cart;
use App\Models\Order;
use App\Models\OrderItem;
use App\Services\InventoryService; // Use the service
use Illuminate\Http\Request;
use Illuminate\Support\Facades\Auth;
use Stripe\Stripe;
use Stripe\Checkout\Session as StripeCheckoutSession;
use Illuminate\Support\Str;
use Illuminate\View\View;
use Illuminate\Http\RedirectResponse;
use Exception;


class CheckoutController extends Controller
{
    protected InventoryService $inventoryService;

    public function __construct(InventoryService $inventoryService)
    {
        $this->middleware('auth'); // Ensure user is logged in
        $this->inventoryService = $inventoryService;
    }

    // Display checkout page (collect address, etc.)
    public function index(): View | RedirectResponse
    {
        if (Cart::count() === 0) {
            return redirect()->route('cart.index')->with('info', 'Your cart is empty.');
        }
        // Pass necessary data (user info, cart total) to the view
        return view('checkout.index');
    }

    // Process checkout and redirect to Stripe
    public function process(Request $request): RedirectResponse
    {
         // 1. Validate request data (address, etc.) if collected on our site
         // $validated = $request->validate([...]);

         if (Cart::count() === 0) {
            return redirect()->route('cart.index')->with('info', 'Your cart is empty.');
        }

        Stripe::setApiKey(config('services.stripe.secret'));

        $lineItems = [];
        foreach (Cart::content() as $item) {
            $lineItems[] = [
                'price_data' => [
                    'currency' => 'usd', // Or your store's currency
                    'product_data' => [
                        'name' => $item->name,
                        // 'images' => [$item->options->image_url ?? asset('images/placeholder.png')], // Optional image
                    ],
                    'unit_amount' => $item->price * 100, // Price in cents
                ],
                'quantity' => $item->qty,
            ];
        }

        try {
            $checkoutSession = StripeCheckoutSession::create([
                'payment_method_types' => ['card'],
                'line_items' => $lineItems,
                'mode' => 'payment',
                'success_url' => route('checkout.success') . '?session_id={CHECKOUT_SESSION_ID}', // Pass session ID
                'cancel_url' => route('checkout.cancel'),
                'customer_email' => Auth::user()->email, // Pre-fill email
                'metadata' => [ // Store relevant info for webhook/success handling
                    'user_id' => Auth::id(),
                    // 'cart_details' => json_encode(Cart::content()), // Be mindful of size limits
                ],
            ]);

            // Store session ID temporarily if needed (e.g., in user session)
            // session(['stripe_checkout_session_id' => $checkoutSession->id]);

            return redirect()->away($checkoutSession->url);

        } catch (Exception $e) {
            // Log error
            report($e);
            return back()->with('error', 'Could not initiate checkout. Please try again later.');
        }
    }

    // Handle successful payment return from Stripe
    public function success(Request $request): View | RedirectResponse
    {
        // Basic success check - Ideally use Stripe Webhooks for reliability
        if (!$request->has('session_id')) {
            return redirect()->route('home')->with('error', 'Invalid checkout session.');
        }

        Stripe::setApiKey(config('services.stripe.secret'));

        try {
            $checkoutSession = StripeCheckoutSession::retrieve($request->get('session_id'));

             // Check if payment was successful (important!)
            if ($checkoutSession->payment_status !== 'paid') {
                 return redirect()->route('checkout.cancel')->with('error', 'Payment was not successful.');
            }

            // Prevent duplicate order creation if user refreshes page
            $existingOrder = Order::where('stripe_payment_id', $checkoutSession->id)->first();
            if ($existingOrder) {
                 return view('checkout.success', ['order' => $existingOrder]); // Show existing order success page
            }

            // Retrieve user_id from metadata or session
            $userId = $checkoutSession->metadata->user_id ?? Auth::id(); // Fallback to logged-in user
             if (!$userId) {
                 throw new Exception("User ID not found in Stripe metadata.");
            }

            // ** CRITICAL SECTION - Use DB Transaction **
            $order = DB::transaction(function () use ($checkoutSession, $userId) {
                // 1. Create Order
                 $order = Order::create([
                    'user_id' => $userId,
                    'order_number' => 'SCENT-' . strtoupper(Str::random(8)), // Generate unique order number
                    'total_amount' => $checkoutSession->amount_total / 100, // Amount from Stripe session
                    'status' => 'processing', // Or 'pending' if further checks needed
                    'stripe_payment_id' => $checkoutSession->id,
                    // 'shipping_address' => ..., // Get from request/session/user profile
                    // 'billing_address' => ...,
                ]);

                // 2. Retrieve cart details (Need a reliable way - session, metadata, cache)
                 // For now, assuming cart state is available (might be fragile)
                if (Cart::count() === 0) throw new Exception("Cart is empty during success handling.");

                // 3. Create Order Items
                foreach (Cart::content() as $item) {
                    OrderItem::create([
                        'order_id' => $order->id,
                        'product_id' => $item->id,
                        'quantity' => $item->qty,
                        'price_at_purchase' => $item->price,
                    ]);
                }

                 // 4. Decrease Stock
                 $this->inventoryService->decreaseStock($order);

                 return $order;
            });

            // 5. Clear Cart
            Cart::destroy();

            // 6. Send Order Confirmation Email (Queue this job)
            // Mail::to(Auth::user())->send(new OrderConfirmationMail($order));
            // dispatch(new SendOrderConfirmationEmailJob($order));


            return view('checkout.success', compact('order'));

        } catch (InsufficientStockException $e) {
            // Handle stock error - refund payment? Notify admin?
             report($e);
            // Attempt to refund via Stripe API here if possible
            return redirect()->route('cart.index')->with('error', $e->getMessage() . ' Your order could not be completed.');
        } catch (Exception $e) {
            report($e);
            // Generic error - might need manual investigation/refund
            return redirect()->route('home')->with('error', 'An error occurred processing your order after payment. Please contact support.');
        }
    }


    // Handle cancelled payment return from Stripe
    public function cancel(): View
    {
        return view('checkout.cancel');
    }

     // ** Stripe Webhook Handler (Highly Recommended) **
     // Create a separate controller/route for handling webhooks like 'checkout.session.completed'
     // This provides a more reliable way to confirm payment and create orders,
     // independent of the user's browser returning to the success URL.
}
```

## 6. Frontend Implementation (Blade, CSS, JS)

### 6.1 Templating Engine (Blade)

*   Utilize Laravel Blade for dynamic HTML generation (`.blade.php` files).
*   Use layouts (`@extends`), sections (`@section`, `@yield`), components (`@component` or class-based components), and includes (`@include`) for reusable UI elements.
*   Employ Blade directives (`@if`, `@foreach`, `@auth`, `@csrf`, etc.) for control structures and security.

```blade
{{-- Example: resources/views/layouts/app.blade.php --}}
<!DOCTYPE html>
<html lang="{{ str_replace('_', '-', app()->getLocale()) }}">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta name="csrf-token" content="{{ csrf_token() }}"> {{-- For AJAX requests --}}

    <title>@yield('title', 'The Scent - Aromatherapy')</title>

    <!-- Fonts -->
    <link rel="preconnect" href="https://fonts.bunny.net">
    <link href="https://fonts.bunny.net/css?family=figtree:400,500,600&display=swap" rel="stylesheet" />
    <link href="https://fonts.googleapis.com/css2?family=Lora:ital,wght@0,400;0,700;1,400&family=Open+Sans:wght@300;400;600&display=swap" rel="stylesheet">

    <!-- Styles -->
    {{-- Link to compiled CSS (Vite or Mix) --}}
    @vite(['resources/css/app.css', 'resources/js/app.js']) {{-- Example using Vite --}}
    {{-- <link rel="stylesheet" href="{{ asset('css/app.css') }}"> --}}
    @yield('styles') {{-- Placeholder for page-specific styles --}}
</head>
<body class="font-sans antialiased">
    <div class="min-h-screen bg-gray-100 dark:bg-gray-900">
        @include('layouts.navigation') {{-- Include navigation bar --}}

        <!-- Page Heading -->
        @hasSection('header')
            <header class="bg-white dark:bg-gray-800 shadow">
                <div class="max-w-7xl mx-auto py-6 px-4 sm:px-6 lg:px-8">
                    @yield('header')
                </div>
            </header>
        @endif

        <!-- Page Content -->
        <main>
            {{-- Display session messages --}}
            @if (session('success')) <div class="alert alert-success">{{ session('success') }}</div> @endif
            @if (session('error')) <div class="alert alert-danger">{{ session('error') }}</div> @endif

            @yield('content') {{-- Main content area --}}
        </main>

         @include('layouts.footer') {{-- Include footer --}}
    </div>

    @yield('scripts') {{-- Placeholder for page-specific scripts --}}
</body>
</html>
```

### 6.2 Styling (CSS/SCSS)

*   Use plain CSS3 or a preprocessor like SCSS for more organized and maintainable styles.
*   Employ a build tool (Laravel Vite or Mix) to compile assets, handle vendor prefixing, and minify CSS for production.
*   Follow a naming convention (e.g., BEM) or use a utility-first framework like Tailwind CSS (integrated with Breeze/Jetstream) for consistency.
*   Define CSS variables (`:root`) for the color palette (e.g., `--primary-color: #3a5a40; --secondary-color: #588157;`) to align with the brand.

```css
/* Example: resources/css/app.css (or app.scss) */
:root {
    --primary-color: #3a5a40;   /* Deep Green */
    --secondary-color: #588157; /* Medium Green */
    --accent-color: #a3b18a;    /* Light Green/Beige */
    --light-bg: #f8f6f4;       /* Off-white/Light Beige */
    --card-bg: #ffffff;
    --text-color: #333333;
    --light-text: #f8f6f4;
    --footer-bg: #344e41;      /* Darker Green */
    --font-heading: 'Lora', serif;
    --font-body: 'Open Sans', sans-serif;
}

body {
    font-family: var(--font-body);
    color: var(--text-color);
    background-color: var(--light-bg);
    line-height: 1.7;
}

h1, h2, h3 {
    font-family: var(--font-heading);
    color: var(--primary-color);
}

.button-primary {
    display: inline-block;
    padding: 10px 25px;
    background-color: var(--secondary-color);
    color: var(--light-text);
    border: none;
    border-radius: 5px;
    text-decoration: none;
    cursor: pointer;
    transition: background-color 0.3s ease;
}

.button-primary:hover {
    background-color: var(--primary-color);
}

/* Styles for product grid, cards, etc. */
.product-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 30px;
    padding: 40px;
    max-width: 1200px;
    margin: 0 auto;
}

.product-card {
    background: var(--card-bg);
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.05);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.product-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 25px rgba(0, 0, 0, 0.1);
}

/* Responsive adjustments */
@media (max-width: 768px) {
    .product-grid {
        grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
        padding: 20px;
        gap: 20px;
    }
}
```

### 6.3 Interactivity (JavaScript ES6+)

*   Use modern JavaScript (ES6+) for frontend interactions.
*   Employ a build tool (Vite/Mix) for compiling, bundling, and minifying JS.
*   Utilize libraries like:
    *   **AOS (Animate On Scroll):** For subtle scroll-triggered animations.
    *   **Alpine.js (Optional):** For simple component interactivity directly in Blade templates.
    *   **Vue.js / React (Optional - Larger Scope):** For complex, dynamic UI components if needed (e.g., advanced filtering, live cart updates).
    *   **Axios (Optional):** For making AJAX requests (or use the native `fetch` API).
*   Implement features like image galleries/zoom for product details, Quick View modals, and potentially AJAX-based cart updates.

```javascript
// Example: resources/js/app.js (Main JS entry point)

// Import necessary libraries
import './bootstrap'; // Often includes Axios, CSRF setup
import AOS from 'aos';
import 'aos/dist/aos.css'; // Import AOS styles

// Initialize AOS
AOS.init({
  duration: 1000, // values from 0 to 3000, with step 50ms
  once: true,     // whether animation should happen only once - while scrolling down
});

// Example: Quick View Modal Logic (Simplified)
document.querySelectorAll('.quick-view-btn').forEach(button => {
    button.addEventListener('click', async (event) => {
        const productId = event.target.dataset.productId;
        const modal = document.getElementById('quick-view-modal');
        const modalContent = modal.querySelector('.modal-content-area');

        modalContent.innerHTML = '<p>Loading...</p>'; // Show loading state
        modal.style.display = 'flex'; // Show modal

        try {
            // Fetch product data via AJAX
            const response = await fetch(`/api/products/${productId}/quick-view`); // Example API endpoint
            if (!response.ok) throw new Error('Failed to load product data');
            const data = await response.json();

            // Populate modal content
            modalContent.innerHTML = `
                <img src="${data.image_url}" alt="${data.name}" class="w-full h-64 object-cover mb-4">
                <h3 class="text-xl font-bold mb-2">${data.name}</h3>
                <p class="text-lg text-gray-800 mb-4">$${data.price}</p>
                <p class="text-sm text-gray-600 mb-4">${data.description.substring(0, 150)}...</p>
                <a href="/products/${data.slug}" class="button-secondary">View Full Details</a>
                <button data-product-id="${data.id}" class="button-primary add-to-cart-quickview ml-2">Add to Cart</button>
            `;
        } catch (error) {
            console.error("Quick View Error:", error);
            modalContent.innerHTML = '<p>Could not load product details. Please try again.</p>';
        }
    });
});

// Add event listener for closing the modal
// Add event listener for Add to Cart within the modal (using event delegation if needed)

// Example: CSRF Token Setup for AJAX (if not handled by bootstrap.js)
// Add to <head>: <meta name="csrf-token" content="{{ csrf_token() }}">
/*
fetch('/some/api/endpoint', {
    method: 'POST',
    headers: {
        'Content-Type': 'application/json',
        'X-CSRF-TOKEN': document.querySelector('meta[name="csrf-token"]').getAttribute('content')
    },
    body: JSON.stringify({ key: 'value' })
});
*/
```

### 6.4 Key UI Components & "Wow Effect"

*   **Hero Section:** Engaging visual (high-quality image, subtle video, or potential future 3D element) with clear value proposition and CTA. Use AOS for entrance animations.
*   **Product Cards:** Display key info (image, name, price, rating). Implement hover effects (lift, shadow) and include "Quick View" and "Add to Cart" buttons. Use provided product images.
*   **Product Grid:** Responsive grid layout using CSS Grid or Flexbox.
*   **Product Detail Page:** Multiple high-resolution images (gallery/slider), potentially zoom functionality, detailed description, specifications, reviews section, clear "Add to Cart" button with quantity selector.
*   **Quick View Modal:** Allows users to see basic product info and add to cart without leaving the catalog page. Triggered from product cards.
*   **Animations:** Use AOS or similar libraries sparingly for smooth transitions and highlighting elements on scroll, enhancing the calming and premium feel.

### 6.5 Responsive Design

*   Implement a mobile-first approach.
*   Use relative units (em, rem, %) where appropriate.
*   Employ CSS Flexbox and Grid for flexible layouts.
*   Use media queries (`@media`) to adjust layout, font sizes, and navigation for different screen sizes (e.g., collapsing navigation into a hamburger menu on mobile).
*   Test thoroughly on various devices and screen resolutions.

## 7. Security Measures

### 7.1 Authentication & Authorization

*   Use Laravel's built-in authentication (Breeze/Jetstream) providing login, registration, password reset.
*   Implement role-based access control (RBAC) using the `role` column in the `users` table and the `AdminMiddleware`.

### 7.2 Data Validation & Sanitization

*   Validate **all** incoming data (user input, API requests) on the server-side using Laravel's Validation (Form Requests preferred).
*   Sanitize output displayed in HTML using Blade's default escaping (`{{ $variable }}`) to prevent XSS. Use `{!! $variable !!}` only for intentionally unescaped HTML and ensure the source is trusted/sanitized.

### 7.3 CSRF Protection

*   Utilize Laravel's built-in CSRF protection. Ensure all state-changing requests (POST, PUT, PATCH, DELETE) use forms with the `@csrf` Blade directive or include the `X-CSRF-TOKEN` header in AJAX requests.

### 7.4 XSS Prevention

*   Blade's `{{ }}` syntax automatically escapes output.
*   Sanitize any user-generated content stored in the database that might be displayed as raw HTML (though this should be avoided). Libraries like HTML Purifier can be used if absolutely necessary.

### 7.5 SQL Injection Prevention

*   Use Laravel's Eloquent ORM and Query Builder, which utilize PDO parameter binding by default, preventing SQL injection vulnerabilities. Avoid using raw SQL queries (`DB::raw()`) with unsanitized user input.

### 7.6 Password Hashing

*   Use Laravel's default `Hash` facade (which uses Bcrypt) to securely hash passwords before storing them. Verify passwords using `Hash::check()`.

### 7.7 HTTPS/SSL Encryption

*   Deploy the application exclusively over HTTPS.
*   Obtain and configure an SSL certificate (e.g., using Let's Encrypt via Certbot).
*   Configure Apache to redirect all HTTP traffic to HTTPS.
*   Use Secure cookies (set `SESSION_SECURE_COOKIE=true` in `.env` for production).

### 7.8 Server & File Permissions

*   Set appropriate file permissions on the server. Web server user (`www-data`) should only have write access to necessary directories (`storage`, `bootstrap/cache`). Other files should generally be read-only for the web server. (Refer to Deployment Guide Appendix).

## 8. Testing Strategy

### 8.1 Unit Testing

*   Test individual classes and methods in isolation (Models, Services, simple Controller actions).
*   Use PHPUnit, included with Laravel.
*   Focus on business logic, calculations, and model relationships/scopes.
*   Mock dependencies to isolate the unit under test.

```php
// Example: tests/Unit/ProductTest.php
namespace Tests\Unit;

use Tests\TestCase;
use App\Models\Product;
use App\Models\Review;
use Illuminate\Foundation\Testing\RefreshDatabase;

class ProductTest extends TestCase
{
    use RefreshDatabase;

    /** @test */
    public function it_can_calculate_average_rating_from_approved_reviews()
    {
        $product = Product::factory()->create();
        Review::factory()->create(['product_id' => $product->id, 'rating' => 4, 'is_approved' => true]);
        Review::factory()->create(['product_id' => $product->id, 'rating' => 5, 'is_approved' => true]);
        Review::factory()->create(['product_id' => $product->id, 'rating' => 3, 'is_approved' => false]); // Unapproved

        // Reload the product to potentially refresh relationships if needed, or access directly
        $this->assertEquals(4.5, $product->average_rating);
    }

     /** @test */
    public function average_rating_is_null_if_no_approved_reviews_exist()
    {
        $product = Product::factory()->create();
        Review::factory()->create(['product_id' => $product->id, 'rating' => 3, 'is_approved' => false]);

        $this->assertNull($product->average_rating);
    }
}
```

### 8.2 Feature Testing

*   Test application features from the user's perspective by making HTTP requests to the application.
*   Use PHPUnit and Laravel's testing helpers (`$this->get()`, `$this->post()`, etc.).
*   Test key user flows: registration, login, adding to cart, checkout, viewing products, admin actions.
*   Assert against response status, view data, database state, session content, redirects.

```php
// Example: tests/Feature/CartTest.php
namespace Tests\Feature;

use Illuminate\Foundation\Testing\RefreshDatabase;
use Tests\TestCase;
use App\Models\Product;
use App\Models\User;
use Gloudemans\Shoppingcart\Facades\Cart; // Use the facade

class CartTest extends TestCase
{
    use RefreshDatabase;

    /** @test */
    public function a_product_can_be_added_to_the_cart()
    {
        $product = Product::factory()->create(['stock' => 10]);
        $user = User::factory()->create(); // Adding to cart might not require auth depending on flow

        $response = $this->actingAs($user) // Or just $this->post(...) if auth not needed
                      ->post(route('cart.add', $product->id));

        $response->assertRedirect(route('cart.index'));
        $response->assertSessionHas('success'); // Check for success message

        // Assert cart content using the package's facade
        $this->assertEquals(1, Cart::count());
        $this->assertEquals($product->name, Cart::content()->first()->name);
    }

    /** @test */
    public function adding_out_of_stock_product_to_cart_fails()
    {
         $product = Product::factory()->create(['stock' => 0]);
         $user = User::factory()->create();

         $response = $this->actingAs($user)->post(route('cart.add', $product->id));

         $response->assertRedirect(); // Should redirect back
         $response->assertSessionHas('error', 'Sorry, this product is out of stock.');
         $this->assertEquals(0, Cart::count());
    }

     /** @test */
    public function cart_item_quantity_can_be_updated()
    {
        $product = Product::factory()->create(['stock' => 10]);
        // Add item first
        Cart::add(['id' => $product->id, 'name' => $product->name, 'qty' => 1, 'price' => $product->price, 'weight' => 0]);
        $cartItem = Cart::content()->first();

        $response = $this->patch(route('cart.update', $cartItem->rowId), ['quantity' => 3]);

        $response->assertRedirect(route('cart.index'));
        $response->assertSessionHas('success');
        $this->assertEquals(3, Cart::get($cartItem->rowId)->qty);
    }
}
```

### 8.3 Manual Testing

*   Perform thorough manual testing on different browsers (Chrome, Firefox, Safari, Edge) and devices (desktop, tablet, mobile).
*   Test critical paths, edge cases, UI/UX issues, and responsiveness.
*   Conduct User Acceptance Testing (UAT) with stakeholders if applicable.

### 8.4 Tools

*   **PHPUnit:** Core testing framework.
*   **Laravel Dusk (Optional):** For browser automation testing, simulating real user interactions in Chrome.
*   **Code Coverage Tools (phpdbg/pcov/Xdebug):** Measure test coverage (`php artisan test --coverage`).
*   **Static Analysis (PHPStan/Psalm - Optional):** Catch potential errors without running code.

## 9. Deployment Strategy

*(Refer to Appendix A for a detailed step-by-step guide)*

### 9.1 Environment Setup (LAMP Stack)

*   Provision a server (e.g., Ubuntu 22.04/24.04 LTS).
*   Install Apache2, MySQL 8.0, PHP 8.2, Composer, Node.js/NPM, Git, Redis.
*   Secure MySQL installation (`mysql_secure_installation`).
*   Configure PHP extensions (`php-mysql`, `php-mbstring`, `php-xml`, `php-curl`, `php-redis`, `php-gd` - if image manipulation needed).

### 9.2 Deployment Process

1.  **Clone Repository:** `git clone <repository_url> /var/www/the-scent`
2.  **Install Dependencies:** `composer install --optimize-autoloader --no-dev`, `npm install && npm run build` (or `npm run prod`)
3.  **Configure Environment:** Copy `.env.example` to `.env`, generate `APP_KEY` (`php artisan key:generate`), fill in database credentials, Stripe keys, Redis info, set `APP_ENV=production`, `APP_DEBUG=false`.
4.  **Database Setup:** Create database and user, run migrations (`php artisan migrate --force`). Seed initial data if necessary (`php artisan db:seed`).
5.  **Set Permissions:** Adjust ownership (`chown -R www-data:www-data`) and permissions (`chmod -R 775 storage bootstrap/cache`).
6.  **Optimize Laravel:** Clear caches (`cache:clear`, `config:clear`, etc.), then cache configuration (`config:cache`, `route:cache`, `view:cache`). Run `php artisan optimize`.
7.  **Configure Web Server:** Set up Apache virtual host (see below).
8.  **Install SSL:** Use Certbot to obtain and configure Let's Encrypt certificate.
9.  **Setup Cron Job:** Add Laravel scheduler task to system crontab.
10. **Setup Redis:** Ensure Redis server is running and enabled. Configure Laravel to use Redis for caching/sessions in `.env`.

### 9.3 Server Configuration (Apache2)

*   Create a virtual host file (`/etc/apache2/sites-available/the-scent.conf`).
*   Configure `DocumentRoot` to `/var/www/the-scent/public`.
*   Set `AllowOverride All` within the `<Directory>` block to allow `.htaccess` (though minimizing `.htaccess` use is better for performance if possible).
*   Enable necessary Apache modules (`rewrite`, `ssl`, `headers`, `deflate`).
*   Enable the site (`a2ensite the-scent.conf`) and restart Apache.
*   Certbot will typically modify the virtual host configuration to handle SSL (*:443) and redirects.

```apache
# Example: /etc/apache2/sites-available/the-scent.conf (before Certbot)
<VirtualHost *:80>
    ServerName the-scent.yourdomain.com
    # ServerAlias www.the-scent.yourdomain.com # Optional

    DocumentRoot /var/www/the-scent/public

    <Directory /var/www/the-scent/public>
        Options Indexes FollowSymLinks
        AllowOverride All
        Require all granted
    </Directory>

    ErrorLog ${APACHE_LOG_DIR}/the-scent_error.log
    CustomLog ${APACHE_LOG_DIR}/the-scent_access.log combined

    # Optional: Add headers for security/performance
    # <IfModule mod_headers.c>
    #    Header set X-Frame-Options "SAMEORIGIN"
    #    Header set X-Content-Type-Options "nosniff"
    #    # Add others like Strict-Transport-Security after HTTPS is set up
    # </IfModule>

</VirtualHost>

# Certbot will create/modify a similar block for <VirtualHost *:443>
```

### 9.4 Post-Deployment Verification

*   Check site accessibility via HTTPS.
*   Test key user flows (registration, login, browsing, cart, checkout).
*   Verify admin panel access and functionality.
*   Check server logs (`apache2`, `laravel.log`) for errors.
*   Test database connection (`php artisan tinker` -> `DB::connection()->ping()`).
*   Test Redis connection (`php artisan tinker` -> `Redis::ping()`).
*   Verify cron job is running (`php artisan schedule:list`).

## 10. Performance Optimization

*(Refer to Appendix C for a checklist)*

### 10.1 Caching Strategy (Redis)

*   **Configuration/Route/View Caching:** Use `php artisan config:cache`, `route:cache`, `view:cache` in production.
*   **Application Cache:** Use Redis as the cache driver (`CACHE_DRIVER=redis` in `.env`). Cache expensive database queries, computed data, external API calls using `Cache::remember()`.
*   **Session Cache:** Use Redis for session storage (`SESSION_DRIVER=redis` in `.env`) for better scalability than file-based sessions.
*   **Object Caching:** Cache frequently accessed Eloquent models or query results. Implement cache tagging for efficient invalidation.
*   **Queue Driver (Future):** Use Redis as the queue driver (`QUEUE_CONNECTION=redis`) for processing background jobs (emails, notifications, image processing).

### 10.2 Database Optimization

*   **Indexing:** Ensure appropriate indexes are created on columns used in `WHERE`, `JOIN`, `ORDER BY` clauses (see [Section 4.2](#42-table-definitions--rationale)). Analyze slow queries (`EXPLAIN`).
*   **Eager Loading:** Prevent N+1 query problems by using Eloquent's eager loading (`with()`) when accessing relationships in loops or views.
*   **Query Optimization:** Write efficient queries. Select only necessary columns (`select()`). Avoid querying inside loops. Use database transactions for atomic operations.
*   **Database Server Tuning:** Optimize MySQL configuration (`my.cnf`) based on server resources (memory, CPU).

### 10.3 Frontend Optimization

*   **Asset Bundling & Minification:** Use Vite/Mix to compile, bundle, and minify CSS and JS files.
*   **Image Optimization:** Compress images (use tools like TinyPNG/ImageOptim). Use appropriate formats (WebP for modern browsers, JPG for photos, PNG for transparency). Implement responsive images (`srcset`). Lazy-load below-the-fold images.
*   **Code Splitting:** Split JS bundles to load code only when needed (supported by Vite/Mix).
*   **Reduce HTTP Requests:** Combine CSS/JS files (handled by bundlers), use CSS sprites or SVG icons.
*   **Browser Caching:** Configure Apache to set appropriate `Cache-Control` and `Expires` headers for static assets. Use ETag headers.
*   **CDN (Future):** Serve static assets (CSS, JS, Images) from a Content Delivery Network for faster global delivery.

### 10.4 Server-Side Optimization

*   **PHP OPcache:** Ensure OPcache is enabled and properly configured in `php.ini` to cache precompiled PHP bytecode.
*   **Gzip Compression:** Enable Gzip/Brotli compression in Apache (`mod_deflate`) to reduce the size of text-based assets (HTML, CSS, JS, JSON).
*   **Keep-Alive:** Ensure Apache's Keep-Alive is enabled for persistent connections.
*   **Server Resources:** Monitor CPU, RAM, Disk I/O and upgrade server resources if bottlenecks are identified.

## 11. Monitoring and Maintenance

### 11.1 Logging

*   **Laravel Logs:** Configure logging levels in `.env` (`LOG_LEVEL`). Monitor `storage/logs/laravel.log`. Use different log channels (e.g., Slack, database) for critical errors if needed.
*   **Apache Logs:** Monitor access (`the-scent_access.log`) and error logs (`the-scent_error.log`).
*   **MySQL Logs:** Enable slow query log to identify performance bottlenecks.

### 11.2 Monitoring Tools

*   **Laravel Telescope (Dev/Staging):** Useful for debugging requests, queries, cache operations, jobs, etc. (`composer require laravel/telescope --dev`). Use with caution in production due to performance overhead.
*   **Server Monitoring:** Use tools like `htop`, `vmstat`, `iostat` or integrated solutions (e.g., Datadog, New Relic, Prometheus+Grafana - Future) to monitor CPU, RAM, Disk, Network usage.
*   **Uptime Monitoring:** Use external services (e.g., UptimeRobot, Pingdom) to monitor site availability.
*   **Error Tracking:** Integrate services like Sentry or Bugsnag for real-time error reporting and aggregation.

### 11.3 Backup Strategy

*   **Database Backups:** Schedule regular (e.g., daily) backups of the MySQL database using `mysqldump`. Store backups securely off-site (e.g., S3, Dropbox). Test restoration periodically.
*   **File Backups:** Schedule regular backups of the application code (`/var/www/the-scent`, excluding `vendor` and cache/log files) and user-uploaded files (if stored locally in `storage/app/public`). Store off-site.
*   **Retention Policy:** Define how long backups are kept.

### 11.4 Scheduled Tasks (Cron)

*   Configure the system cron daemon to run Laravel's scheduler every minute (`* * * * * cd /path-to-your-project && php artisan schedule:run >> /dev/null 2>&1`).
*   Define scheduled tasks within `app/Console/Kernel.php` (e.g., cleanup tasks, sending summary reports, updating order statuses).

## 12. Conclusions and Recommendations

### 12.1 Summary

This document outlines the technical design for "The Scent" e-commerce platform, built on Apache2, PHP 8.2 (Laravel 10), and MySQL 8.0. The design prioritizes a secure, performant, and user-friendly experience aligned with the company's mission of promoting well-being through aromatherapy. Key features include a robust product catalog, secure Stripe checkout, admin management capabilities, and a focus on visual appeal and interactivity.

### 12.2 Future Enhancements

1.  **Phase 2 Features:**
    *   Advanced Search (potentially Algolia integration).
    *   Wishlist Functionality.
    *   Discount Codes & Promotions Module.
    *   Automated Email Notifications (Order Confirmation, Shipping Updates - using Queues).
    *   Blog/Content Section for aromatherapy articles.
    *   Social Login Integration.
2.  **Long-term Enhancements:**
    *   AI-Powered Product Recommendations.
    *   Multi-language / Multi-currency Support.
    *   Dedicated Mobile App (iOS/Android - potentially using API).
    *   Subscription Box Feature.
    *   Integration with Shipping APIs (e.g., Shippo, EasyPost).
    *   Enhanced Admin Analytics & Reporting.
    *   Full WCAG AA Accessibility Compliance.
    *   Implement CDN for static assets.

## Appendix A: Detailed Deployment Guide

*(This section summarizes the steps from `deploy_guide.md` and `design_specification_document.md`, adapted for the chosen stack)*

**Target Environment:** Ubuntu 22.04/24.04 LTS, Apache2, MySQL 8.0, PHP 8.2, Redis, Node.js, Composer, Git

1.  **Server Preparation:**
    *   Update system: `sudo apt update && sudo apt upgrade -y`
    *   Install Apache, PHP & extensions, MySQL, Redis, Certbot, Git, Composer, Node/NPM.
        ```bash
        sudo apt install apache2 php8.2 libapache2-mod-php php8.2-mysql php8.2-mbstring php8.2-xml php8.2-curl php8.2-redis php8.2-gd php8.2-zip mysql-server redis-server git composer nodejs npm certbot python3-certbot-apache -y
        ```
    *   Secure MySQL: `sudo mysql_secure_installation`
    *   Enable Apache modules: `sudo a2enmod rewrite ssl headers deflate`
    *   Start/Enable services: `sudo systemctl enable --now apache2 mysql redis-server`

2.  **Database Setup:**
    *   Login to MySQL: `sudo mysql -u root -p`
    *   Create database and user:
        ```sql
        CREATE DATABASE the_scent_db CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
        CREATE USER 'the_scent_user'@'localhost' IDENTIFIED BY 'YOUR_SECURE_PASSWORD';
        GRANT ALL PRIVILEGES ON the_scent_db.* TO 'the_scent_user'@'localhost';
        FLUSH PRIVILEGES;
        EXIT;
        ```

3.  **Application Deployment:**
    *   Clone repo: `sudo git clone <repository_url> /var/www/the-scent`
    *   Navigate to project dir: `cd /var/www/the-scent`
    *   Install PHP dependencies: `sudo composer install --optimize-autoloader --no-dev`
    *   Install JS dependencies & build assets: `sudo npm install && sudo npm run build`
    *   Set up `.env` file:
        *   `sudo cp .env.example .env`
        *   Generate key: `sudo php artisan key:generate --force`
        *   Edit `.env` with database credentials, app URL, Stripe keys, Redis details, mail settings, set `APP_ENV=production`, `APP_DEBUG=false`, `SESSION_DRIVER=redis`, `CACHE_DRIVER=redis`, `SESSION_SECURE_COOKIE=true`.
    *   Run migrations: `sudo php artisan migrate --force` (Use `--seed` if seeders exist)
    *   Set Permissions:
        ```bash
        sudo chown -R $USER:www-data /var/www/the-scent # Set user ownership first if needed
        sudo chown -R www-data:www-data /var/www/the-scent/storage /var/www/the-scent/bootstrap/cache
        sudo find /var/www/the-scent -type f -exec chmod 644 {} \;
        sudo find /var/www/the-scent -type d -exec chmod 755 {} \;
        sudo chmod -R ug+w /var/www/the-scent/storage /var/www/the-scent/bootstrap/cache # Give group write access too
        ```
    *   Optimize Laravel:
        ```bash
        sudo php artisan cache:clear
        sudo php artisan config:clear
        sudo php artisan route:clear
        sudo php artisan view:clear
        sudo php artisan config:cache
        sudo php artisan route:cache
        sudo php artisan view:cache
        sudo php artisan optimize
        ```

4.  **Web Server Configuration:**
    *   Create Apache vHost: `sudo nano /etc/apache2/sites-available/the-scent.conf` (Use content from [Section 9.3](#93-server-configuration-apache2), replacing `the-scent.yourdomain.com` with actual domain)
    *   Enable site: `sudo a2ensite the-scent.conf`
    *   Test Apache config: `sudo apache2ctl configtest`
    *   Restart Apache: `sudo systemctl restart apache2`

5.  **SSL Certificate Setup:**
    *   Run Certbot: `sudo certbot --apache -d the-scent.yourdomain.com` (Follow prompts, choose redirect option)
    *   Test auto-renewal: `sudo certbot renew --dry-run` (Certbot adds its own cron/systemd timer)

6.  **Cron Job Setup:**
    *   Edit crontab: `sudo crontab -e`
    *   Add scheduler line: `* * * * * cd /var/www/the-scent && /usr/bin/php artisan schedule:run >> /dev/null 2>&1` (Ensure correct path to php)

7.  **Post-Deployment Verification:** (As described in [Section 9.4](#94-post-deployment-verification))

## Appendix B: Code Repository Structure

```plaintext
the-scent/
├── app/
│   ├── Console/         # Artisan commands (e.g., Kernel.php)
│   ├── Exceptions/      # Custom Exception classes, Handler.php
│   ├── Http/
│   │   ├── Controllers/ # Route handling logic (e.g., ProductController.php)
│   │   │   └── Admin/   # Controllers specific to Admin section
│   │   ├── Middleware/  # Request filtering (e.g., AdminMiddleware.php)
│   │   └── Requests/    # Form Request validation classes
│   ├── Jobs/            # Queued jobs (e.g., SendOrderConfirmationEmailJob.php)
│   ├── Listeners/       # Event listeners
│   ├── Mail/            # Mailable classes (e.g., OrderConfirmationMail.php)
│   ├── Models/          # Eloquent Models (e.g., Product.php, User.php)
│   ├── Providers/       # Service Providers (AppServiceProvider, AuthServiceProvider, etc.)
│   ├── Rules/           # Custom validation rules
│   └── Services/        # Business logic services (e.g., InventoryService.php)
├── bootstrap/           # Framework bootstrap scripts, cache directory
│   └── cache/
├── config/              # Configuration files (database.php, app.php, services.php)
├── database/
│   ├── factories/       # Model factories (e.g., ProductFactory.php)
│   ├── migrations/      # Database migration files
│   └── seeders/         # Database seeder files (DatabaseSeeder.php)
├── public/              # Publicly accessible files (Document Root)
│   ├── css/             # Compiled CSS files
│   ├── js/              # Compiled JS files
│   ├── images/          # Static images (logo, icons), potentially product images symlink
│   ├── storage/         # Symlink to storage/app/public
│   ├── index.php        # Entry point
│   └── .htaccess        # Apache rewrite rules
├── resources/
│   ├── css/             # Source SCSS/CSS files
│   ├── js/              # Source JS files (app.js, components)
│   ├── lang/            # Language translation files
│   └── views/           # Blade template files
│       ├── admin/       # Views for the admin section
│       ├── auth/        # Auth views (login, register)
│       ├── cart/        # Cart view
│       ├── checkout/    # Checkout views (index, success, cancel)
│       ├── emails/      # Email templates
│       ├── layouts/     # Base layout files (app.blade.php)
│       ├── products/    # Product listing and detail views
│       └── components/  # Reusable Blade components
├── routes/              # Route definitions
│   ├── api.php          # API routes
│   ├── channels.php     # Broadcasting channels
│   ├── console.php      # Console command routes
│   └── web.php          # Web interface routes
├── storage/             # Application storage
│   ├── app/             # Application specific files
│   │   └── public/      # Publicly accessible user uploads (symlinked to public/storage)
│   ├── framework/       # Cached files (sessions, views, cache)
│   └── logs/            # Application log files (laravel.log)
├── tests/               # Automated tests
│   ├── Browser/         # Laravel Dusk tests (Optional)
│   ├── Feature/         # Feature tests (e.g., CartTest.php)
│   └── Unit/            # Unit tests (e.g., ProductTest.php)
├── vendor/              # Composer dependencies (ignored by Git)
├── .editorconfig        # Editor configuration
├── .env                 # Environment variables (ignored by Git)
├── .env.example         # Example environment file
├── .gitattributes       # Git attributes
├── .gitignore           # Files/directories ignored by Git
├── artisan              # Laravel CLI tool
├── composer.json        # PHP dependencies manifest
├── composer.lock        # Locked PHP dependency versions
├── package.json         # Node.js dependencies manifest
├── package-lock.json    # Locked Node.js dependency versions
├── phpunit.xml          # PHPUnit configuration
└── vite.config.js       # Vite build tool configuration (or webpack.mix.js for Laravel Mix)
```

## Appendix C: Performance Optimization Checklist

**Backend / Laravel:**
*   [x] Enable OPcache in `php.ini`.
*   [x] Use `php artisan config:cache`.
*   [x] Use `php artisan route:cache`.
*   [x] Use `php artisan view:cache`.
*   [x] Use `php artisan optimize` (combines above caches).
*   [x] Implement Redis/Memcached for application caching (`Cache::remember`).
*   [x] Implement Redis/Memcached for session storage.
*   [x] Use Eager Loading (`with()`) to prevent N+1 queries.
*   [x] Select only necessary columns in database queries.
*   [ ] Offload slow tasks (email, image processing) to Queues (Redis driver recommended).
*   [ ] Analyze slow database queries (`EXPLAIN`, slow query log).
*   [x] Ensure proper database indexing.

**Frontend / Assets:**
*   [x] Use Vite/Mix for asset bundling and minification (CSS, JS).
*   [x] Optimize images (compression, appropriate formats like WebP).
*   [x] Implement responsive images (`srcset`).
*   [ ] Implement lazy loading for images/iframes below the fold.
*   [ ] Implement code splitting for large JS bundles.
*   [ ] Analyze frontend performance (Lighthouse, WebPageTest).
*   [ ] Reduce unused CSS/JS.
*   [ ] Defer loading non-critical JavaScript.

**Server / Network:**
*   [x] Enable Gzip/Brotli compression (Apache `mod_deflate`).
*   [x] Configure browser caching headers (`Cache-Control`, `Expires`) for static assets via Apache.
*   [x] Ensure HTTP Keep-Alive is enabled.
*   [ ] Use a Content Delivery Network (CDN) for static assets.
*   [ ] Optimize web server configuration (Apache workers/threads).
*   [ ] Optimize database server configuration (`my.cnf`).
*   [ ] Ensure sufficient server resources (CPU, RAM, IO).

---
This comprehensive document provides a solid foundation for building "The Scent" e-commerce platform. Remember to replace placeholders (like `YOUR_SECURE_PASSWORD`, `the-scent.yourdomain.com`) with actual values during implementation.  
