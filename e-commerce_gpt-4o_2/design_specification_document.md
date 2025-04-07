This document will serve as a **blueprint** for developers, maintainers, and technical reviewers. It will include:

---

### 📄 STRUCTURE OF THE TECHNICAL DESIGN SPECIFICATION

1. **Introduction**
   - Project overview
   - Design goals & objectives
   - Target users and business use case

2. **Design Methodology & Approach**
   - Design philosophies used (modularity, separation of concerns, reusability)
   - Tools and technologies
   - Security, scalability, and maintainability considerations

3. **System Architecture**
   - High-level architecture
   - Client-server interaction
   - MVC pattern usage (if applicable)

4. **Detailed Component Design**
   - Frontend design (HTML, CSS, JS)
   - Backend logic (PHP)
   - Database schema (MySQL)
   - Stripe integration
   - Email notifications
   - AJAX cart system
   - Search and filter logic
   - Language and currency modules
   - Admin panel
   - Security design (CSRF, validation, session management)

5. **Code Snippets & Explanations**
   - Key code excerpts with detailed walkthroughs
   - Best practices, error handling

6. **Deployment Strategy**
   - Local and production deployment
   - File structure
   - Hosting environment

7. **Conclusion**
   - Summary of system capabilities
   - Strengths and areas of improvement

8. **Recommendations**
   - Future enhancements
   - Security hardening
   - Migration paths (e.g., to Laravel or microservices)

---

✅ I will now begin writing the **full 6000+ word Technical Design Specification Document** for _The Scent_ E-Commerce Platform. This will be a very large document and will be written in structured sections over several responses due to formatting and system limits.

</think>

---

# 🛠️ THE SCENT E-COMMERCE PLATFORM  
### Technical Design Specification Document  
**Version:** 1.0  
**Author:** ChatGPT  
**Date:** 2025-04-07  
**Word Count Target:** 6000+  

---

## 1. Introduction

### 1.1 Project Overview

**The Scent** is a premium aromatherapy e-commerce platform that enables customers to browse, customize, and purchase a wide range of essential oils and handmade natural soaps. The platform combines a luxurious brand aesthetic with modern e-commerce functionality, creating a holistic user experience that promotes wellness and mindfulness.

This project was developed using the **Apache2 + PHP + MySQL** stack, with **vanilla HTML/CSS/JS** on the frontend and secure, modular PHP on the backend. It includes an admin portal for managing products and orders, and a customer portal for account management and order history.

---

### 1.2 Design Goals & Objectives

- Support **global customer base** with multi-language and multi-currency capabilities.
- Provide a seamless **shopping experience** with real-time cart updates, product filtering, and Stripe payment integration.
- Ensure **security and data integrity** through CSRF protection, input validation, and secure session handling.
- Allow **admin users** to manage inventory, view orders, and update content.
- Be easily **deployable** to shared hosting, VPS, or cloud platforms.
- Remain **framework-free** for simplicity, but structured for future migration to Laravel or similar.

---

### 1.3 Target Users and Use Case

- **End Customers**: Browse products, filter by scent or category, add to cart, pay via Stripe, and track order history.
- **Admin Team**: Manage product catalog, view and fulfill orders, and update descriptions or pricing as needed.

---

## 2. Design Methodology & Approach

### 2.1 Development Philosophy

This system was built using several guiding principles:

- **Modularity**: Code is broken into reusable components (e.g., `db.php`, `lang.php`, `exchange-rate.php`).
- **Separation of Concerns**: Clear distinction between business logic (PHP), presentation (HTML/CSS), and interaction (JavaScript).
- **Progressive Enhancement**: The system works without JS, but enhances UX with AJAX for cart management.
- **Security First**: Input sanitization, CSRF tokens, and secure password hashing are applied consistently.

---

### 2.2 Tools and Technologies Used

| Component | Technology |
|----------|------------|
| Server   | Apache2    |
| Backend  | PHP 8.x    |
| Database | MySQL 8.x  |
| Frontend | HTML5, CSS3, JS |
| Payment  | Stripe Checkout (SDK) |
| Email    | PHP `mail()` or SMTP (PHPMailer-ready) |
| i18n     | PHP associative arrays |
| Currency | exchangerate.host API |

---

### 2.3 Security, Scalability, Maintainability

- **Security**: All inputs are sanitized; sessions are used securely; admin area is protected.
- **Scalability**: While the platform uses flat PHP, the code structure allows future migration to MVC frameworks (Laravel).
- **Maintainability**: Code is organized into logical folders, and uses consistent naming and commenting practices.

---

## 3. System Architecture

### 3.1 High-Level Architecture

```plaintext
+-------------------+            +---------------------+
|   Client (Browser)| <--------> |     Apache Server   |
+-------------------+            |  (PHP + HTML + JS)  |
                                 +----------+----------+
                                            |
                                            v
                                 +---------------------+
                                 |     MySQL Database  |
                                 +---------------------+
```

---

### 3.2 MVC-Like Separation

While not a full MVC framework, the system approximates MVC:

- **Model**: `db.php`, SQL queries, and logic in `checkout.php`, `cart.php`, etc.
- **View**: HTML templates like `index.php`, `product.php`
- **Controller**: Form handling scripts, AJAX endpoints (`add-to-cart.php`)

---

### 3.3 Data Flow (Example: Checkout)

1. User submits checkout form
2. Backend validates CSRF token & sanitizes data
3. Inserts order into `orders` table
4. Inserts products into `order_items`
5. Sends confirmation email
6. Redirects to `thankyou.php`

---

**[Next Part →]**

In the next message, I will continue with:

## 4. Detailed Component Design  
- Frontend (HTML/CSS/JS)  
- Backend (PHP)  
- Database schema  
- Stripe payment  
- Email notifications  
- Admin portal  
- AJAX cart  
- Language & currency modules  
- Security features  

Each with **code samples and in-depth explanations**.

---

🧱 **Next Up**: Full walkthrough of all components, including code and architectural decisions.  
💬 I will now continue in the next message due to space limits.
