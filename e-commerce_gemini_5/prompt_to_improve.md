Okay, I understand the goal: transform the provided basic HTML/CSS into a visually stunning, premium, and calming landing page for "The Scent," incorporating specific "Wow Effect" elements based on the outlined plan. I will focus on layout, typography, color, imagery integration (using the provided placeholders), and subtle interactions to achieve this.

Here is the improved HTML (`index.html`) and CSS (`style.css`) code:

**`index.html` (Improved Version)**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Scent - Evoke Calm | Premium Aromatherapy & Natural Well-being</title> <!-- Enhanced Title -->

    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,600;0,700;1,400&family=Montserrat:wght@300;400;500;600&family=Raleway:wght@400;500;600&display=swap" rel="stylesheet">

    <!-- Font Awesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" integrity="sha512-iecdLmaskl7CVkqkXNQ/ZH/XLlvWZOJyj7Yy7tcenmpD1ypASozpmT/E0iPtmFIB46ZmdtAc9eNBvH0H/ZpiBw==" crossorigin="anonymous" referrerpolicy="no-referrer" />

    <!-- Link to Your CSS -->
    <link rel="stylesheet" href="style.css">

    <!-- Favicon Placeholder (replace with actual favicon links) -->
    <link rel="icon" href="/favicon.ico" sizes="any">
    <link rel="icon" href="/favicon.svg" type="image/svg+xml">
    <link rel="apple-touch-icon" href="/apple-touch-icon.png">

</head>
<body>

    <!-- Header -->
    <header class="main-header">
        <div class="container header-container">
            <div class="logo">
                <a href="#">The Scent</a>
                <span>NATURAL WELL-BEING</span> <!-- Slightly modified tagline -->
            </div>
            <nav class="main-nav">
                <ul>
                    <li><a href="#hero">Home</a></li>
                    <li><a href="#philosophy">Philosophy</a></li>
                    <li><a href="#products">Shop</a></li>
                    <li><a href="#finder">Discover</a></li>
                    <!-- Optional Story link could go here -->
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
            <div class="header-icons">
                <a href="#" aria-label="Search"><i class="fas fa-search"></i></a>
                <a href="#" aria-label="Account"><i class="fas fa-user-circle"></i></a> <!-- Slightly different icon -->
                <a href="#" aria-label="Cart"><i class="fas fa-shopping-bag"></i></a>
            </div>
             <button class="mobile-nav-toggle" aria-label="Toggle navigation" aria-expanded="false">
                <i class="fas fa-bars"></i>
                <i class="fas fa-times"></i> <!-- Add close icon -->
            </button>
        </div>
         <!-- Mobile Menu (hidden by default) -->
        <nav class="mobile-nav">
            <ul>
                <li><a href="#hero">Home</a></li>
                <li><a href="#philosophy">Philosophy</a></li>
                <li><a href="#products">Shop</a></li>
                <li><a href="#finder">Discover</a></li>
                <li><a href="#contact">Contact</a></li>
                 <li class="mobile-nav-divider"><hr></li>
                 <li><a href="#">Search</a></li>
                <li><a href="#">Account</a></li>
                <li><a href="#">Cart</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <!-- Hero Section -->
        <section id="hero" class="hero-section">
            <div class="hero-background">
                <!-- Background image/video set in CSS -->
                <div class="hero-overlay"></div> <!-- Separate overlay div -->
            </div>
            <div class="container hero-content">
                <h1 class="hero-title">Find Your Moment <br><em>of Calm</em></h1> <!-- Italic emphasis -->
                <p class="hero-subtitle">Elevate your senses and restore balance with our meticulously crafted, natural aromatherapy essentials.</p>
                <a href="#products" class="btn btn-primary btn-hero">Explore Collections</a>
            </div>
             <a href="#philosophy" class="scroll-down-indicator" aria-label="Scroll down">
                <i class="fas fa-chevron-down"></i>
            </a>
        </section>

        <!-- Philosophy/Mission Section -->
        <section id="philosophy" class="philosophy-section">
            <div class="container philosophy-container">
                <div class="philosophy-image-wrapper">
                     <img src="https://raw.githubusercontent.com/nordeim/The-Scent/refs/heads/main/images/scent6.jpg" alt="Artisanal arrangement of natural ingredients like herbs and oils">
                     <!-- Optional: Add a subtle graphic element behind/around image -->
                     <!-- <div class="image-accent"></div> -->
                </div>
                <div class="philosophy-text">
                    <h2 class="section-title">Rooted in Nature,<br>Crafted with Heart</h2>
                    <p>At The Scent, we believe true well-being blossoms from a connection to nature. We meticulously source the purest botanical ingredients from ethical global partners, blending ancient aromatherapy wisdom with modern understanding. Our passion is creating harmonious, effective blends that support your journey towards mental clarity, physical ease, and everyday serenity.</p>
                    <p><em>Experience the difference purity makes.</em></p> <!-- Added emphasis -->
                    <a href="#" class="btn btn-secondary">Our Story & Values</a>
                </div>
            </div>
        </section>

        <!-- Featured Products Section -->
        <section id="products" class="products-section">
            <div class="container">
                <h2 class="section-title text-center">Curated Essentials</h2>
                <p class="section-subtitle text-center">Discover signature blends designed for your well-being.</p>
                <div class="product-grid">
                    <!-- Product 1: Essential Oil -->
                    <div class="product-card">
                        <div class="product-image-container">
                            <img src="https://raw.githubusercontent.com/nordeim/The-Scent/refs/heads/main/images/scent2.jpg" alt="Serenity Blend Essential Oil bottle">
                            <a href="#" class="btn-quick-view" aria-label="Quick View Serenity Blend Oil">Quick View</a>
                        </div>
                        <div class="product-info">
                            <h3>Serenity Blend Oil</h3>
                            <p>Calming Lavender & Chamomile</p>
                            <span class="product-price">$28.00</span> <!-- Added Price -->
                            <a href="#" class="product-link">View Details</a>
                        </div>
                    </div>
                    <!-- Product 2: Soap -->
                    <div class="product-card">
                         <div class="product-image-container">
                            <img src="https://raw.githubusercontent.com/nordeim/The-Scent/refs/heads/main/images/soap4.jpg" alt="Handcrafted Citrus Burst Soap bar">
                             <a href="#" class="btn-quick-view" aria-label="Quick View Citrus Burst Soap">Quick View</a>
                        </div>
                        <div class="product-info">
                            <h3>Citrus Burst Soap</h3>
                            <p>Energizing Lemon & Orange Peel</p>
                             <span class="product-price">$12.50</span> <!-- Added Price -->
                            <a href="#" class="product-link">View Details</a>
                        </div>
                    </div>
                    <!-- Product 3: Essential Oil -->
                     <div class="product-card">
                        <div class="product-image-container">
                            <img src="https://raw.githubusercontent.com/nordeim/The-Scent/refs/heads/main/images/scent4.jpg" alt="Focus Flow Essential Oil bottle">
                             <a href="#" class="btn-quick-view" aria-label="Quick View Focus Flow Oil">Quick View</a>
                         </div>
                        <div class="product-info">
                            <h3>Focus Flow Oil</h3>
                            <p>Invigorating Rosemary & Mint</p>
                            <span class="product-price">$26.00</span> <!-- Added Price -->
                            <a href="#" class="product-link">View Details</a>
                        </div>
                    </div>
                     <!-- Product 4: Soap -->
                    <div class="product-card">
                         <div class="product-image-container">
                            <img src="https://raw.githubusercontent.com/nordeim/The-Scent/refs/heads/main/images/soap6.jpg" alt="Woodland Retreat natural Soap bar">
                            <a href="#" class="btn-quick-view" aria-label="Quick View Woodland Retreat Soap">Quick View</a>
                        </div>
                         <div class="product-info">
                            <h3>Woodland Retreat Soap</h3>
                            <p>Grounding Cedarwood & Pine</p>
                            <span class="product-price">$13.00</span> <!-- Added Price -->
                            <a href="#" class="product-link">View Details</a>
                        </div>
                    </div>
                </div>
                 <div class="view-all-cta">
                     <a href="#" class="btn btn-primary">Shop All Collections</a>
                 </div>
            </div>
        </section>

        <!-- Scent Finder Section -->
        <section id="finder" class="finder-section">
            <!-- Optional subtle background pattern/texture -->
            <div class="container">
                <h2 class="section-title text-center">Discover Your Scent Profile</h2>
                <p class="section-subtitle text-center">Let intuition guide you. Select the mood you wish to cultivate.</p>
                <div class="finder-grid">
                    <a href="#" class="finder-card relaxation"> <!-- Added class for potential specific styling -->
                        <div class="finder-icon-wrapper">
                            <i class="fas fa-leaf finder-icon"></i>
                        </div>
                        <h3>Relaxation</h3>
                        <p>Unwind & De-stress</p>
                    </a>
                    <a href="#" class="finder-card energy">
                         <div class="finder-icon-wrapper">
                            <i class="fas fa-bolt finder-icon"></i>
                         </div>
                        <h3>Energy</h3>
                        <p>Invigorate & Uplift</p>
                    </a>
                     <a href="#" class="finder-card focus">
                         <div class="finder-icon-wrapper">
                            <i class="fas fa-brain finder-icon"></i>
                         </div>
                        <h3>Focus</h3>
                        <p>Clarity & Concentration</p>
                    </a>
                     <a href="#" class="finder-card sleep">
                         <div class="finder-icon-wrapper">
                             <i class="fas fa-moon finder-icon"></i>
                        </div>
                        <h3>Sleep</h3>
                        <p>Restful & Serene</p>
                     </a>
                    <a href="#" class="finder-card balance">
                        <div class="finder-icon-wrapper">
                           <i class="fas fa-balance-scale finder-icon"></i>
                         </div>
                        <h3>Balance</h3>
                        <p>Center & Harmonize</p>
                     </a>
                     <!-- Add one more for better grid fill potentially -->
                     <a href="#" class="finder-card custom">
                         <div class="finder-icon-wrapper">
                            <i class="fas fa-vial finder-icon"></i> <!-- Example Icon -->
                         </div>
                        <h3>Custom Blends</h3>
                        <p>Explore Possibilities</p>
                    </a>
                </div>
                <div class="finder-cta">
                    <p>Ready for a deeper dive?</p>
                    <a href="#" class="btn btn-secondary btn-finder">Take the Full Scent Quiz</a>
                </div>
            </div>
        </section>

         <!-- Testimonials Section -->
        <section id="testimonials" class="testimonials-section">
            <div class="container">
                <h2 class="section-title text-center">Whispers of Well-being</h2>
                <p class="section-subtitle text-center">Hear from our cherished community.</p>
                 <div class="testimonial-grid">
                     <!-- Using blockquote for semantic meaning -->
                    <blockquote class="testimonial-card">
                        <div class="testimonial-rating">★★★★★</div>
                        <p>"The Serenity Blend oil is pure magic in a bottle. It's become an essential part of my evening ritual. Truly calming and the quality is exceptional."</p>
                        <cite class="testimonial-author">- Alexandra V.</cite>
                    </blockquote>
                     <blockquote class="testimonial-card">
                        <div class="testimonial-rating">★★★★★</div>
                        <p>"I adore the Woodland Retreat soap! The scent is grounding, it lathers beautifully, and my skin feels incredibly soft without any dryness. Highly recommend."</p>
                         <cite class="testimonial-author">- David R.</cite>
                    </blockquote>
                    <blockquote class="testimonial-card">
                         <div class="testimonial-rating">★★★★★</div>
                         <p>"Finally, a natural soap that smells divine and doesn't irritate my sensitive skin. The Citrus Burst is so uplifting in my morning shower!"</p>
                         <cite class="testimonial-author">- Megan S.</cite>
                    </blockquote>
                </div>
            </div>
        </section>

        <!-- Newsletter Section -->
        <section id="newsletter" class="newsletter-section">
             <div class="newsletter-background"></div> <!-- For potential image/gradient -->
            <div class="container newsletter-container">
                 <i class="fas fa-envelope-open-text newsletter-icon"></i> <!-- Added icon -->
                 <h2 class="section-title">Join the Circle</h2>
                 <p class="section-subtitle">Subscribe for mindful moments, exclusive insights, and 10% off your first order.</p>
                <form class="newsletter-form">
                    <input type="email" placeholder="Enter your email address" required aria-label="Email address for newsletter">
                    <button type="submit" class="btn btn-primary btn-newsletter">Subscribe</button>
                </form>
                 <p class="newsletter-consent">We respect your privacy. Unsubscribe anytime.</p>
            </div>
        </section>

    </main>

    <!-- Footer -->
    <footer id="contact" class="main-footer">
        <div class="container footer-grid">
            <div class="footer-about">
                <h3 class="footer-title logo"><a href="#">The Scent</a></h3> <!-- Re-use logo style -->
                <p>Crafting moments of calm and clarity through the power of pure aromatherapy.</p>
                 <div class="social-icons">
                    <a href="#" aria-label="Facebook"><i class="fab fa-facebook-f"></i></a>
                    <a href="#" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
                    <a href="#" aria-label="Pinterest"><i class="fab fa-pinterest-p"></i></a> <!-- Changed icon -->
                    <a href="#" aria-label="TikTok"><i class="fab fa-tiktok"></i></a> <!-- Added TikTok -->
                </div>
            </div>
             <div class="footer-links">
                <h3 class="footer-title">Explore</h3>
                <ul>
                    <li><a href="#philosophy">Our Philosophy</a></li>
                    <li><a href="#">Ingredients</a></li>
                    <li><a href="#">Blog</a></li>
                    <li><a href="#">Sustainability</a></li>
                    <li><a href="#">Gift Cards</a></li>
                </ul>
            </div>
            <div class="footer-links">
                <h3 class="footer-title">Support</h3>
                 <ul>
                    <li><a href="#">Contact Us</a></li>
                    <li><a href="#">FAQ</a></li>
                    <li><a href="#">Shipping & Returns</a></li>
                    <li><a href="#">My Account</a></li>
                    <li><a href="#">Terms & Privacy</a></li>
                </ul>
            </div>
             <div class="footer-contact">
                 <h3 class="footer-title">Get in Touch</h3>
                 <!-- Removed icons for cleaner look, implied by context -->
                <p>123 Aromatherapy Lane,<br>Wellness City, WB 12345</p>
                <p><a href="tel:+15551234567">+1 (555) 123-4567</a></p>
                <p><a href="mailto:hello@thescent.com">hello@thescent.com</a></p>
            </div>
        </div>
        <div class="footer-bottom">
            <div class="container footer-bottom-container">
                <p>&copy; <span id="current-year"></span> The Scent. Cultivating Well-being, Naturally.</p>
                 <div class="payment-methods">
                     <!-- Using text or SVGs for payment icons is often preferred -->
                    <span>Secure Payments By:</span>
                     <i class="fab fa-cc-visa" title="Visa"></i>
                    <i class="fab fa-cc-mastercard" title="Mastercard"></i>
                    <i class="fab fa-cc-paypal" title="PayPal"></i>
                    <i class="fab fa-cc-amex" title="American Express"></i>
                    <i class="fab fa-cc-discover" title="Discover"></i> <!-- Added Discover -->
                 </div>
            </div>
        </div>
    </footer>

    <!-- Back to Top Button (Optional) -->
    <!-- <a href="#hero" class="back-to-top" aria-label="Back to top"><i class="fas fa-arrow-up"></i></a> -->

    <script>
        // --- Mobile Menu Toggle ---
        const toggleButton = document.querySelector('.mobile-nav-toggle');
        const mobileNav = document.querySelector('.mobile-nav');
        const mainHeader = document.querySelector('.main-header');
        const body = document.body; // Get body element

        if (toggleButton && mobileNav && mainHeader) {
            toggleButton.addEventListener('click', () => {
                const isExpanded = toggleButton.getAttribute('aria-expanded') === 'true';
                toggleButton.setAttribute('aria-expanded', !isExpanded);
                mobileNav.classList.toggle('active');
                mainHeader.classList.toggle('mobile-menu-active');
                body.classList.toggle('no-scroll'); // Prevent scrolling when menu is open

                // Toggle icon visibility (alternative to changing class)
                toggleButton.querySelector('.fa-bars').style.display = isExpanded ? 'block' : 'none';
                toggleButton.querySelector('.fa-times').style.display = isExpanded ? 'none' : 'block';
            });

             // Close menu when a link is clicked
            mobileNav.querySelectorAll('a').forEach(link => {
                link.addEventListener('click', () => {
                     mobileNav.classList.remove('active');
                     mainHeader.classList.remove('mobile-menu-active');
                     body.classList.remove('no-scroll');
                     toggleButton.setAttribute('aria-expanded', 'false');
                     // Reset icons
                     toggleButton.querySelector('.fa-bars').style.display = 'block';
                     toggleButton.querySelector('.fa-times').style.display = 'none';
                });
            });
        }

         // --- Sticky Header ---
         let lastScrollY = window.scrollY;
        window.addEventListener('scroll', () => {
            if (window.scrollY > 50) {
                 mainHeader.classList.add('sticky');
                 // Optional: Hide header on scroll down, show on scroll up
                 if (window.scrollY > lastScrollY) {
                    // mainHeader.classList.add('hide-on-scroll'); // Add this class in CSS if desired
                 } else {
                    // mainHeader.classList.remove('hide-on-scroll');
                 }
            } else {
                mainHeader.classList.remove('sticky');
                // mainHeader.classList.remove('hide-on-scroll');
             }
             lastScrollY = window.scrollY; // Update last scroll position
        });

        // --- Set Current Year in Footer ---
         const currentYearSpan = document.getElementById('current-year');
         if (currentYearSpan) {
            currentYearSpan.textContent = new Date().getFullYear();
         }

         // --- Simple Fade-In Animation on Scroll (using Intersection Observer) ---
        const animatedElements = document.querySelectorAll('.philosophy-image-wrapper, .philosophy-text, .product-card, .finder-card, .testimonial-card, .newsletter-container');

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                    // Optional: Unobserve after animation to save resources
                    // observer.unobserve(entry.target);
                }
                // Optional: Remove class if element scrolls out of view
                // else {
                //     entry.target.classList.remove('visible');
                // }
            });
        }, {
            threshold: 0.1 // Trigger when 10% of the element is visible
        });

        animatedElements.forEach(el => {
            observer.observe(el);
        });

    </script>

</body>
</html>
```

**`style.css` (Improved Version)**

```css
/* --- Base Styles & Variables --- */
:root {
    --font-heading: 'Cormorant Garamond', serif;
    --font-body: 'Montserrat', sans-serif;
    --font-accent: 'Raleway', sans-serif;

    /* Refined Palette - slightly more muted and sophisticated */
    --color-primary: #2C3E50; /* Deeper Slate Blue/Grey */
    --color-primary-dark: #1F2B38; /* Darker shade for footer */
    --color-secondary: #A0BCC1; /* Softer, slightly desaturated Mint/Blue */
    --color-accent: #C8A070; /* Muted Gold/Bronze */
    --color-accent-light: #E8D5BB; /* Lighter accent for backgrounds */
    --color-background: #FDFBF8; /* Warmer, subtle Off-White */
    --color-background-alt: #FFFFFF; /* Pure White for contrast */
    --color-text: #424242; /* Slightly softer dark grey */
    --color-text-light: #FDFBF8; /* Matches warm background */
    --color-border: #e0e0e0;
    --color-success: #5cb85c; /* For potential form feedback */
    --color-error: #d9534f; /* For potential form feedback */

    --container-width: 1200px;
    --container-padding: 2rem; /* More generous padding */
    --spacing-unit: 1rem; /* Approx 16px */
    --border-radius: 6px; /* Softer radius */
    --border-radius-pill: 50px;

    --shadow-light: 0 4px 15px rgba(0, 0, 0, 0.04);
    --shadow-medium: 0 8px 25px rgba(0, 0, 0, 0.08);
    --shadow-dark: 0 10px 30px rgba(0, 0, 0, 0.12);

    --transition-speed: 0.4s; /* Slightly slower for elegance */
    --transition-ease: cubic-bezier(0.25, 0.8, 0.25, 1); /* Smoother ease */
}

*, *::before, *::after {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

html {
    scroll-behavior: smooth;
    font-size: 100%; /* 16px base */
    -webkit-font-smoothing: antialiased; /* Smoother fonts on WebKit */
    -moz-osx-font-smoothing: grayscale; /* Smoother fonts on Firefox */
}

body {
    font-family: var(--font-body);
    color: var(--color-text);
    background-color: var(--color-background);
    line-height: 1.7;
    overflow-x: hidden; /* Prevent horizontal scroll */
}

/* Prevent body scroll when mobile menu is open */
body.no-scroll {
    overflow: hidden;
}


h1, h2, h3, h4, h5, h6 {
    font-family: var(--font-heading);
    font-weight: 600;
    color: var(--color-primary);
    margin-bottom: calc(var(--spacing-unit) * 1.2);
    line-height: 1.3;
}

/* Responsive Typography */
h1 { font-size: clamp(2.5rem, 6vw, 4.2rem); font-weight: 700; }
h2.section-title { font-size: clamp(2rem, 5vw, 3.2rem); } /* Specific class for consistency */
h3 { font-size: clamp(1.3rem, 4vw, 1.9rem); }
h4 { font-size: clamp(1.1rem, 3vw, 1.5rem); }

p {
    margin-bottom: calc(var(--spacing-unit) * 1.5);
    max-width: 65ch; /* Slightly adjusted */
}
/* Subtitle specific styling */
.section-subtitle {
    font-family: var(--font-accent);
    font-size: clamp(1rem, 2.5vw, 1.2rem);
    color: var(--color-text);
    opacity: 0.8;
    max-width: 70ch;
    margin-left: auto;
    margin-right: auto;
    margin-top: calc(var(--spacing-unit) * -0.5); /* Pull closer to title */
    margin-bottom: calc(var(--spacing-unit) * 3);
}


a {
    color: var(--color-primary);
    text-decoration: none;
    transition: color var(--transition-speed) var(--transition-ease);
}

a:hover, a:focus {
    color: var(--color-accent);
    outline: 2px solid transparent; /* Basic focus outline */
    outline-offset: 2px;
}
a:focus-visible { /* More visible focus for keyboard nav */
     outline-color: var(--color-accent);
}

img {
    max-width: 100%;
    height: auto;
    display: block;
    border-radius: var(--border-radius); /* Default soft radius */
}

ul { list-style: none; }
em { font-style: italic; } /* Ensure italic renders */
cite { font-style: normal; } /* Reset cite style */

.container {
    width: 90%;
    max-width: var(--container-width);
    margin: 0 auto;
    padding: 0 var(--container-padding);
}

.text-center { text-align: center; }

/* Basic Scroll Fade-in Animation Setup */
.philosophy-image-wrapper, .philosophy-text,
.product-card, .finder-card, .testimonial-card,
.newsletter-container {
    opacity: 0;
    transform: translateY(30px);
    transition: opacity 0.8s var(--transition-ease), transform 0.8s var(--transition-ease);
}

.visible {
    opacity: 1;
    transform: translateY(0);
}


/* --- Buttons --- */
.btn {
    display: inline-block;
    font-family: var(--font-accent);
    font-weight: 600; /* Slightly bolder */
    text-transform: uppercase;
    letter-spacing: 1px; /* More spacing */
    padding: calc(var(--spacing-unit) * 0.9) calc(var(--spacing-unit) * 2.5); /* Slightly larger */
    border-radius: var(--border-radius-pill);
    cursor: pointer;
    transition: background-color var(--transition-speed) var(--transition-ease),
                color var(--transition-speed) var(--transition-ease),
                transform var(--transition-speed) var(--transition-ease),
                box-shadow var(--transition-speed) var(--transition-ease);
    border: 2px solid transparent;
    text-align: center;
    line-height: 1.4; /* Ensure text fits */
}

.btn-primary {
    background-color: var(--color-primary);
    color: var(--color-text-light);
    border-color: var(--color-primary);
}

.btn-primary:hover, .btn-primary:focus {
    background-color: var(--color-accent);
    border-color: var(--color-accent);
    color: var(--color-primary-dark); /* Contrast on gold */
    transform: translateY(-3px);
    box-shadow: var(--shadow-medium);
}

.btn-secondary {
    background-color: transparent;
    color: var(--color-primary);
    border-color: var(--color-secondary); /* Use softer border */
}

.btn-secondary:hover, .btn-secondary:focus {
    background-color: var(--color-primary);
    border-color: var(--color-primary);
    color: var(--color-text-light);
     transform: translateY(-3px);
     box-shadow: var(--shadow-light);
}
/* Specific Button Adjustments */
.btn-hero { padding: calc(var(--spacing-unit) * 1) calc(var(--spacing-unit) * 3); font-size: 1.1rem; }
.btn-newsletter { background-color: var(--color-accent); border-color: var(--color-accent); color: var(--color-primary-dark); }
.btn-newsletter:hover, .btn-newsletter:focus { background-color: var(--color-accent-light); border-color: var(--color-accent-light); color: var(--color-primary); box-shadow: var(--shadow-light);}
.btn-finder { border-color: var(--color-primary); }
.btn-finder:hover, .btn-finder:focus { background-color: var(--color-primary); color: var(--color-text-light); border-color: var(--color-primary); }

/* --- Header --- */
.main-header {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 1000;
    padding: calc(var(--spacing-unit) * 1.5) 0;
    background: transparent;
    transition: background-color var(--transition-speed) var(--transition-ease),
                box-shadow var(--transition-speed) var(--transition-ease),
                padding var(--transition-speed) var(--transition-ease),
                transform var(--transition-speed) var(--transition-ease); /* Added transform transition */
}
.main-header.sticky {
     position: fixed;
     background-color: rgba(255, 255, 255, 0.97); /* High transparency white */
     backdrop-filter: blur(10px); /* Frosted glass effect */
     -webkit-backdrop-filter: blur(10px);
     box-shadow: var(--shadow-light);
     padding: calc(var(--spacing-unit) * 0.8) 0;
}
/* Optional: Hide header on scroll down */
/* .main-header.hide-on-scroll {
    transform: translateY(-100%);
} */

.main-header.sticky .logo a,
.main-header.sticky .main-nav a,
.main-header.sticky .header-icons a,
.main-header.sticky .mobile-nav-toggle {
    color: var(--color-primary);
}
.main-header.sticky .logo span {
    color: var(--color-text);
}
.main-header.sticky .main-nav a:hover,
.main-header.sticky .header-icons a:hover {
    color: var(--color-accent);
}

/* Header Layout */
.header-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

/* Logo */
.logo a {
    font-family: var(--font-heading);
    font-size: clamp(1.6rem, 4vw, 2rem);
    font-weight: 700;
    color: var(--color-text-light); /* White for hero overlay */
    text-transform: uppercase;
    letter-spacing: 1.5px;
    transition: color var(--transition-speed) var(--transition-ease);
}
.logo span {
    display: block;
    font-family: var(--font-accent);
    font-size: 0.6rem;
    letter-spacing: 4px; /* Wider spacing */
    text-transform: uppercase;
    color: var(--color-text-light); /* White for hero overlay */
    margin-top: -8px; /* Adjust overlap */
    opacity: 0.8;
     transition: color var(--transition-speed) var(--transition-ease);
}

/* Desktop Navigation */
.main-nav ul {
    display: flex;
    gap: calc(var(--spacing-unit) * 2.5);
}

.main-nav a {
    font-family: var(--font-accent);
    font-weight: 500;
    color: var(--color-text-light); /* White for hero overlay */
    text-transform: uppercase;
    letter-spacing: 1.2px;
    padding: 8px 4px; /* More clickable area */
    position: relative;
    transition: color var(--transition-speed) var(--transition-ease);
}
/* Underline effect */
.main-nav a::after {
    content: '';
    position: absolute;
    width: 0;
    height: 2px;
    bottom: 0;
    left: 0; /* Start from left */
    background-color: var(--color-accent);
    transition: width var(--transition-speed) var(--transition-ease);
}
.main-nav a:hover::after, .main-nav a:focus::after {
    width: 100%;
}
.main-nav a:hover, .main-nav a:focus {
    color: var(--color-accent); /* Accent color on hover */
}
.main-header.sticky .main-nav a:hover,
.main-header.sticky .main-nav a:focus {
    color: var(--color-accent);
}
.main-header.sticky .main-nav a::after { /* Sticky header underline */
    background-color: var(--color-accent);
}


/* Header Icons */
.header-icons {
    display: flex;
    gap: calc(var(--spacing-unit) * 1.8);
}

.header-icons a {
    color: var(--color-text-light); /* White for hero overlay */
    font-size: 1.3rem; /* Slightly larger icons */
    transition: color var(--transition-speed) var(--transition-ease), transform var(--transition-speed) var(--transition-ease);
}
.header-icons a:hover, .header-icons a:focus {
    color: var(--color-accent);
    transform: scale(1.1);
}

/* Mobile Navigation Toggle */
.mobile-nav-toggle {
    display: none; /* Hidden on desktop */
    background: none;
    border: none;
    color: var(--color-text-light); /* White for hero overlay */
    font-size: 1.6rem;
    cursor: pointer;
    z-index: 1100; /* Above mobile nav content */
    padding: 5px;
     transition: color var(--transition-speed) var(--transition-ease);
}
.mobile-nav-toggle .fa-times { display: none; } /* Hide close icon initially */

.main-header.mobile-menu-active .mobile-nav-toggle {
    color: var(--color-primary); /* Dark color when menu open */
}

/* Mobile Navigation Panel */
.mobile-nav {
    display: block; /* Always block, control visibility with transform/opacity */
    position: fixed; /* Fixed position */
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh; /* Full height */
    background-color: var(--color-background); /* Use body background */
    padding: calc(var(--spacing-unit) * 6) var(--spacing-unit) var(--spacing-unit); /* Top padding for header */
    z-index: 1050; /* Below toggle, above content */
    opacity: 0;
    visibility: hidden;
    transform: translateX(100%); /* Slide in from right */
    transition: opacity var(--transition-speed) var(--transition-ease),
                visibility var(--transition-speed) var(--transition-ease),
                transform var(--transition-speed) var(--transition-ease);
    overflow-y: auto; /* Allow scrolling if content exceeds height */
}
.mobile-nav.active {
     opacity: 1;
     visibility: visible;
     transform: translateX(0);
}

.mobile-nav ul {
    display: flex;
    flex-direction: column;
    gap: var(--spacing-unit) * 0.5; /* Tighter gap */
    text-align: center;
}

.mobile-nav a {
    display: block;
    padding: calc(var(--spacing-unit) * 1);
    color: var(--color-primary);
    font-family: var(--font-accent);
    text-transform: uppercase;
    font-size: 1.3rem; /* Larger font size */
    letter-spacing: 1px;
    transition: background-color var(--transition-speed) var(--transition-ease), color var(--transition-speed) var(--transition-ease);
    border-radius: var(--border-radius);
}
.mobile-nav a:hover, .mobile-nav a:focus {
     background-color: var(--color-secondary);
     color: var(--color-primary);
}
.mobile-nav-divider hr {
    border: none;
    border-top: 1px solid var(--color-border);
    margin: var(--spacing-unit) 0;
}


/* --- Hero Section --- */
.hero-section {
    position: relative;
    height: 100vh; /* Full viewport height */
    min-height: 650px; /* Ensure minimum height */
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    overflow: hidden;
    color: var(--color-text-light);
}

.hero-background {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-image: url('https://raw.githubusercontent.com/nordeim/The-Scent/refs/heads/main/images/scent5.jpg'); /* High-quality image */
    background-size: cover;
    background-position: center 30%; /* Adjust vertical position */
    /* background-attachment: fixed; -- Creates parallax but can be jerky on mobile, consider alternatives */
    z-index: 1;
    /* Subtle zoom animation */
    animation: zoomInOut 30s infinite alternate ease-in-out;
}

.hero-overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    /* Gradient overlay for better text contrast and mood */
    background: linear-gradient(to bottom, rgba(44, 62, 80, 0.3), rgba(44, 62, 80, 0.7)); /* Primary color based */
    z-index: 2;
}

.hero-content {
    position: relative; /* Above overlay */
    z-index: 3;
    max-width: 850px;
    padding: 0 var(--spacing-unit);
    /* Fade-in animation for content */
    animation: fadeInHeroContent 1.5s 0.5s var(--transition-ease) forwards;
    opacity: 0; /* Start hidden */
}

.hero-title {
    color: var(--color-text-light);
    font-weight: 700;
    margin-bottom: calc(var(--spacing-unit) * 0.8);
    text-shadow: 0 2px 10px rgba(0, 0, 0, 0.3); /* Subtle text shadow */
}
.hero-title em {
    font-weight: 400; /* Lighter weight for italic part */
    font-style: italic;
    color: var(--color-accent-light); /* Use light accent */
}

.hero-subtitle {
    font-size: clamp(1.1rem, 3vw, 1.4rem);
    margin-bottom: calc(var(--spacing-unit) * 2.5);
    opacity: 0.95;
    color: var(--color-text-light);
    max-width: 60ch;
    margin-left: auto;
    margin-right: auto;
    font-weight: 300; /* Lighter body font weight */
}

/* Scroll Down Indicator */
.scroll-down-indicator {
    position: absolute;
    bottom: 30px;
    left: 50%;
    transform: translateX(-50%);
    z-index: 3;
    color: var(--color-text-light);
    opacity: 0.7;
    font-size: 1.5rem;
    animation: bounce 2s infinite ease-in-out;
    transition: opacity var(--transition-speed) var(--transition-ease);
}
.scroll-down-indicator:hover {
    opacity: 1;
}

/* Animations */
@keyframes fadeInHeroContent {
    from { opacity: 0; transform: translateY(25px); }
    to { opacity: 1; transform: translateY(0); }
}
@keyframes zoomInOut {
     from { transform: scale(1); }
    to { transform: scale(1.08); } /* Slightly more noticeable zoom */
}
@keyframes bounce {
    0%, 20%, 50%, 80%, 100% { transform: translateX(-50%) translateY(0); }
    40% { transform: translateX(-50%) translateY(-10px); }
    60% { transform: translateX(-50%) translateY(-5px); }
}

/* --- Generic Section Styling --- */
section {
    padding: calc(var(--spacing-unit) * 6) 0; /* More vertical space */
}
/* Alternate background for visual rhythm */
section:nth-child(even) {
    background-color: var(--color-background-alt); /* White background */
}
section .section-title {
    margin-bottom: calc(var(--spacing-unit) * 1); /* Reduced space before subtitle */
}
section .section-title.text-center {
    margin-left: auto;
    margin-right: auto;
}


/* --- Philosophy Section --- */
/* #philosophy { background-color: var(--color-background); } */
.philosophy-container {
    display: grid;
    grid-template-columns: 1fr 1.1fr; /* Slightly asymmetric */
    gap: calc(var(--spacing-unit) * 5);
    align-items: center;
}
.philosophy-image-wrapper {
    position: relative; /* For potential accents */
    /* Animation delay */
    transition-delay: 0.1s;
}
.philosophy-image-wrapper img {
    box-shadow: var(--shadow-medium);
    transition: transform var(--transition-speed) var(--transition-ease), box-shadow var(--transition-speed) var(--transition-ease);
}
.philosophy-image-wrapper:hover img {
    transform: scale(1.03) rotate(-1deg); /* Subtle tilt */
    box-shadow: var(--shadow-dark);
}
/* Optional: Accent shape behind image */
/* .image-accent { ... } */

.philosophy-text {
    /* Animation delay */
    transition-delay: 0.2s;
}
.philosophy-text .section-title {
    text-align: left;
}
.philosophy-text p {
    margin-bottom: calc(var(--spacing-unit) * 1.8);
}
.philosophy-text em {
    color: var(--color-accent); /* Accent color for emphasis */
    font-weight: 500;
}
.philosophy-text .btn-secondary {
     margin-top: var(--spacing-unit);
}

/* --- Products Section --- */
.products-section { background-color: var(--color-background-alt); }
.product-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: calc(var(--spacing-unit) * 3); /* Increased gap */
}
.product-card {
    background-color: var(--color-background); /* Warm off-white card */
    border-radius: var(--border-radius);
    overflow: hidden;
    box-shadow: var(--shadow-light);
    transition: transform var(--transition-speed) var(--transition-ease), box-shadow var(--transition-speed) var(--transition-ease);
    position: relative;
    display: flex;
    flex-direction: column; /* Ensure info stays below image */
    /* Animation delay based on position - needs JS for complex grids */
    /* transition-delay: calc(0.1s * var(--card-index, 1)); */
}
.product-card:hover {
    transform: translateY(-8px); /* More pronounced lift */
    box-shadow: var(--shadow-dark);
}
.product-image-container {
    position: relative; /* For overlay button */
    overflow: hidden; /* Keep image zoom contained */
}
.product-card img {
    width: 100%;
    height: 300px; /* Fixed height */
    object-fit: cover; /* Ensure image covers area */
    transition: transform var(--transition-speed) var(--transition-ease), opacity var(--transition-speed) var(--transition-ease);
    border-radius: var(--border-radius) var(--border-radius) 0 0; /* Only top radius */
}
.product-card:hover img {
    transform: scale(1.05);
    opacity: 0.9;
}
/* Quick View Button */
.btn-quick-view {
    position: absolute;
    bottom: 15px;
    left: 50%;
    transform: translateX(-50%) translateY(10px); /* Start hidden */
    opacity: 0;
    background-color: rgba(44, 62, 80, 0.8); /* Semi-transparent primary */
    color: var(--color-text-light);
    padding: calc(var(--spacing-unit) * 0.5) calc(var(--spacing-unit) * 1.5);
    border-radius: var(--border-radius-pill);
    font-size: 0.8rem;
    font-family: var(--font-accent);
    text-transform: uppercase;
    letter-spacing: 0.5px;
    border: 1px solid rgba(255, 255, 255, 0.5);
    transition: opacity var(--transition-speed) var(--transition-ease), transform var(--transition-speed) var(--transition-ease);
    white-space: nowrap; /* Prevent wrapping */
}
.product-card:hover .btn-quick-view {
    opacity: 1;
    transform: translateX(-50%) translateY(0);
}
.btn-quick-view:hover, .btn-quick-view:focus {
    background-color: var(--color-accent);
    color: var(--color-primary-dark);
    border-color: var(--color-accent);
}

/* Product Info */
.product-info {
    padding: calc(var(--spacing-unit) * 1.8);
    text-align: center;
    flex-grow: 1; /* Allow info to take remaining space */
    display: flex;
    flex-direction: column;
    justify-content: space-between; /* Push link down */
}
.product-info h3 {
    margin-bottom: calc(var(--spacing-unit) * 0.5);
    font-size: 1.4rem;
    font-weight: 600;
}
.product-info p { /* Product description/tagline */
    font-size: 0.95rem;
    color: #666;
    margin-bottom: calc(var(--spacing-unit) * 1);
    flex-grow: 1; /* Allow description to push down price/link if needed */
}
.product-price {
    display: block;
    font-family: var(--font-accent);
    font-size: 1.1rem;
    font-weight: 600;
    color: var(--color-primary);
    margin-bottom: calc(var(--spacing-unit) * 1.2);
}
.product-link {
    font-family: var(--font-accent);
    font-weight: 600;
    color: var(--color-accent);
    text-transform: uppercase;
    font-size: 0.9rem;
    letter-spacing: 0.8px;
    position: relative;
    padding-bottom: 4px;
    align-self: center; /* Center link horizontally */
}
.product-link::after {
    content: '';
    position: absolute;
    width: 0;
    height: 2px;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
    background-color: var(--color-accent);
    transition: width var(--transition-speed) var(--transition-ease);
}
.product-card:hover .product-link::after {
    width: 60%;
}
.view-all-cta {
    text-align: center;
    margin-top: calc(var(--spacing-unit) * 4); /* More space above */
}


/* --- Scent Finder Section --- */
.finder-section {
    background-color: var(--color-accent-light); /* Light accent background */
    position: relative;
    /* Optional: Subtle texture/pattern */
    /* background-image: url('path/to/subtle-texture.png'); */
}
.finder-section .section-title {
     color: var(--color-primary);
}
.finder-section .section-subtitle {
    color: var(--color-primary);
    opacity: 0.9;
}

.finder-grid {
    display: grid;
    /* Aim for 3 columns on desktop, flexible */
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: calc(var(--spacing-unit) * 2.5);
}
.finder-card {
    background-color: rgba(255, 255, 255, 0.6); /* Semi-transparent white */
    backdrop-filter: blur(5px); /* Blur effect */
    -webkit-backdrop-filter: blur(5px);
    padding: calc(var(--spacing-unit) * 2);
    border-radius: var(--border-radius);
    text-align: center;
    transition: background-color var(--transition-speed) var(--transition-ease),
                transform var(--transition-speed) var(--transition-ease),
                box-shadow var(--transition-speed) var(--transition-ease);
    cursor: pointer;
    color: var(--color-primary);
    border: 1px solid rgba(255, 255, 255, 0.8); /* Subtle border */
    display: flex; /* Use flex for better alignment */
    flex-direction: column;
    align-items: center;
    justify-content: center; /* Center content vertically */
    min-height: 200px; /* Ensure consistent height */
}
.finder-card:hover, .finder-card:focus {
    background-color: rgba(255, 255, 255, 0.9);
    transform: translateY(-8px) scale(1.02); /* Lift and slight scale */
    box-shadow: var(--shadow-medium);
    color: var(--color-accent); /* Change text color on hover */
}
.finder-icon-wrapper {
    width: 70px;
    height: 70px;
    background-color: var(--color-text-light); /* White circle */
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-bottom: var(--spacing-unit) * 1.5;
    transition: background-color var(--transition-speed) var(--transition-ease), transform var(--transition-speed) var(--transition-ease);
    box-shadow: var(--shadow-light);
}
.finder-card:hover .finder-icon-wrapper {
    background-color: var(--color-primary); /* Primary color on hover */
    transform: scale(1.1);
}
.finder-icon {
    font-size: 2rem; /* Adjust icon size */
    color: var(--color-primary);
    transition: color var(--transition-speed) var(--transition-ease);
}
.finder-card:hover .finder-icon {
    color: var(--color-text-light); /* Light icon on dark bg */
}
.finder-card h3 {
    font-family: var(--font-accent); /* Use accent font */
    font-size: 1.3rem;
    font-weight: 600;
    margin-bottom: calc(var(--spacing-unit) * 0.3);
    color: inherit; /* Inherit color from card */
}
.finder-card p {
     font-size: 0.9rem;
     line-height: 1.5;
     color: inherit; /* Inherit color from card */
     opacity: 0.8;
     margin-bottom: 0;
}
.finder-cta {
    text-align: center;
    margin-top: calc(var(--spacing-unit) * 4);
}
.finder-cta p {
    margin-bottom: var(--spacing-unit);
    font-family: var(--font-accent);
    font-size: 1.1rem;
    color: var(--color-primary);
}

/* --- Testimonials Section --- */
.testimonials-section { background-color: var(--color-background-alt); }
.testimonial-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: calc(var(--spacing-unit) * 2.5);
}
.testimonial-card {
    background-color: var(--color-background); /* Warm off-white */
    padding: calc(var(--spacing-unit) * 2.5); /* More padding */
    border-radius: var(--border-radius);
    border-top: 5px solid var(--color-secondary); /* Accent border on top */
    box-shadow: var(--shadow-light);
    position: relative; /* For quote icon */
    transition: transform var(--transition-speed) var(--transition-ease), box-shadow var(--transition-speed) var(--transition-ease);
}
.testimonial-card:hover {
     transform: translateY(-5px);
     box-shadow: var(--shadow-medium);
}
/* Optional: Add quote icon */
.testimonial-card::before {
    content: '\f10d'; /* Font Awesome quote-left */
    font-family: 'Font Awesome 6 Free';
    font-weight: 900;
    position: absolute;
    top: 15px;
    left: 20px;
    font-size: 2.5rem;
    color: var(--color-secondary);
    opacity: 0.2;
    z-index: 0;
}

.testimonial-card p {
    font-style: italic;
    margin-bottom: var(--spacing-unit) * 1.5;
    color: #555;
    position: relative; /* Ensure text is above pseudo-element */
    z-index: 1;
    font-size: 1.05rem; /* Slightly larger quote text */
    padding-left: 10px; /* Indent text slightly from quote */
}
.testimonial-author {
    display: block;
    font-weight: 600; /* Bolder author */
    color: var(--color-primary);
    margin-top: var(--spacing-unit);
    text-align: right;
    position: relative; /* Ensure text is above pseudo-element */
    z-index: 1;
    font-family: var(--font-accent);
}
.testimonial-rating {
    color: var(--color-accent);
    font-size: 1.1rem;
    margin-bottom: var(--spacing-unit);
    position: relative; /* Ensure text is above pseudo-element */
    z-index: 1;
    text-align: left;
}

/* --- Newsletter Section --- */
.newsletter-section {
     background-color: var(--color-secondary); /* Use secondary color */
     color: var(--color-primary); /* Dark text */
     padding: calc(var(--spacing-unit) * 5) 0;
     position: relative;
     overflow: hidden;
}
/* Optional decorative background element */
/* .newsletter-background { ... } */
.newsletter-icon {
    font-size: 3rem;
    display: block;
    text-align: center;
    margin-bottom: var(--spacing-unit);
    opacity: 0.8;
}
.newsletter-section .section-title { color: var(--color-primary); }
.newsletter-section .section-subtitle { color: var(--color-primary); opacity: 0.9; }

.newsletter-container {
     text-align: center;
     max-width: 650px;
     position: relative;
     z-index: 1;
}
.newsletter-form {
    display: flex;
    justify-content: center;
    gap: var(--spacing-unit);
    margin-top: calc(var(--spacing-unit) * 2);
    margin-bottom: var(--spacing-unit);
    flex-wrap: wrap; /* Wrap on smaller screens */
}
.newsletter-form input[type="email"] {
    padding: calc(var(--spacing-unit) * 1) calc(var(--spacing-unit) * 1.5);
    border: 1px solid rgba(44, 62, 80, 0.3); /* Primary color border, low opacity */
    border-radius: var(--border-radius-pill);
    font-family: var(--font-body);
    font-size: 1rem;
    min-width: 300px;
    flex-grow: 1; /* Take available space */
    background-color: rgba(255, 255, 255, 0.7); /* Slightly transparent */
    transition: border-color var(--transition-speed) var(--transition-ease), box-shadow var(--transition-speed) var(--transition-ease);
}
.newsletter-form input[type="email"]:focus {
    outline: none;
    border-color: var(--color-accent);
    box-shadow: 0 0 0 3px rgba(200, 160, 112, 0.3); /* Accent glow */
}
.newsletter-consent {
    font-size: 0.85rem;
    opacity: 0.7;
    margin-bottom: 0;
    margin-top: var(--spacing-unit);
}


/* --- Footer --- */
.main-footer {
    background-color: var(--color-primary-dark); /* Darker primary shade */
    color: #b0bec5; /* Lighter grey for text */
    padding-top: calc(var(--spacing-unit) * 5);
    font-size: 0.95rem; /* Slightly larger base font */
}
.footer-grid {
    display: grid;
    /* Flexible columns, aiming for 4 */
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: calc(var(--spacing-unit) * 3);
    margin-bottom: calc(var(--spacing-unit) * 4);
}
.footer-title {
    font-family: var(--font-accent);
    color: var(--color-text-light);
    font-weight: 600;
    margin-bottom: calc(var(--spacing-unit) * 1.5);
    font-size: 1.2rem;
    letter-spacing: 0.5px;
}
/* Use logo style for first column title */
.footer-about .footer-title.logo a {
    font-size: 1.8rem; /* Match header logo size */
    color: var(--color-text-light);
}
.footer-about .footer-title.logo a:hover {
    color: var(--color-accent);
}
.footer-about p {
    line-height: 1.6;
    margin-bottom: calc(var(--spacing-unit) * 1.5);
    opacity: 0.9;
}
.social-icons {
    display: flex;
    gap: calc(var(--spacing-unit) * 1.2);
    margin-top: var(--spacing-unit);
}
.social-icons a {
    color: #b0bec5;
    font-size: 1.4rem; /* Larger icons */
    transition: color var(--transition-speed) var(--transition-ease), transform var(--transition-speed) var(--transition-ease);
}
.social-icons a:hover, .social-icons a:focus {
    color: var(--color-accent);
    transform: scale(1.15) translateY(-2px); /* More noticeable interaction */
}

.footer-links ul li {
    margin-bottom: calc(var(--spacing-unit) * 0.8);
}
.footer-links a {
    color: #b0bec5;
    position: relative;
    padding-bottom: 2px;
}
/* Subtle underline effect for footer links */
.footer-links a::after {
    content: '';
    position: absolute;
    width: 0;
    height: 1px;
    bottom: 0;
    left: 0;
    background-color: var(--color-secondary);
    transition: width var(--transition-speed) var(--transition-ease);
}
.footer-links a:hover, .footer-links a:focus {
    color: var(--color-text-light);
}
.footer-links a:hover::after, .footer-links a:focus::after {
     width: 100%;
}
.footer-contact p {
    margin-bottom: calc(var(--spacing-unit) * 0.8);
    line-height: 1.6;
}
.footer-contact a { /* Make email/phone clickable */
    color: #b0bec5;
    transition: color var(--transition-speed) var(--transition-ease);
}
.footer-contact a:hover, .footer-contact a:focus {
     color: var(--color-text-light);
     text-decoration: underline;
}


.footer-bottom {
    background-color: #1a2530; /* Even darker shade */
    padding: calc(var(--spacing-unit) * 1.5) 0;
    margin-top: calc(var(--spacing-unit) * 3);
    border-top: 1px solid rgba(176, 190, 197, 0.2); /* Subtle top border */
}
.footer-bottom-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: var(--spacing-unit);
    font-size: 0.9rem;
    color: #90a4ae; /* Slightly lighter grey for contrast */
}
.payment-methods {
    display: flex;
    align-items: center;
    gap: calc(var(--spacing-unit) * 0.8);
}
.payment-methods span {
     margin-right: calc(var(--spacing-unit) * 0.5);
     font-size: 0.85rem;
     opacity: 0.8;
}
.payment-methods i {
    font-size: 1.9rem; /* Larger payment icons */
    color: #78909c; /* Mid-grey */
    opacity: 0.7;
    transition: opacity var(--transition-speed) var(--transition-ease);
}
.payment-methods i:hover {
    opacity: 1;
}


/* --- Responsive Design --- */

/* Tablets and smaller desktops (~992px) */
@media (max-width: 992px) {
    :root { --container-padding: 1.5rem; }
    .main-nav { display: none; } /* Hide desktop nav */
    .header-icons { display: none; } /* Hide icons */
    .mobile-nav-toggle { display: block; } /* Show hamburger */

    .philosophy-container {
        grid-template-columns: 1fr; /* Stack */
        gap: calc(var(--spacing-unit) * 3);
        text-align: center;
    }
     .philosophy-image-wrapper {
         order: -1; /* Image first */
         max-width: 500px; /* Limit image width */
         margin: 0 auto calc(var(--spacing-unit) * 2) auto;
     }
    .philosophy-text .section-title { text-align: center; }
    .philosophy-text { text-align: center; }
    .philosophy-text p { margin-left: auto; margin-right: auto; }

    .product-grid { gap: calc(var(--spacing-unit) * 2); }
    .finder-grid { gap: calc(var(--spacing-unit) * 2); }
    .testimonial-grid { gap: calc(var(--spacing-unit) * 2); }
    .footer-grid { grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); }
}

/* Mobile phones (~576px) */
@media (max-width: 576px) {
    :root { --container-padding: 1rem; }
    h1 { font-size: 2.2rem; }
    h2.section-title { font-size: 1.8rem; }
    .section-subtitle { font-size: 1rem; margin-bottom: calc(var(--spacing-unit) * 2); }

    .hero-section { min-height: 550px; }
    .hero-subtitle { font-size: 1rem; }
    .btn { padding: calc(var(--spacing-unit) * 0.8) calc(var(--spacing-unit) * 2); font-size: 0.9rem; letter-spacing: 0.8px;}
    .btn-hero { padding: calc(var(--spacing-unit) * 0.9) calc(var(--spacing-unit) * 2.5); font-size: 1rem; }

    section { padding: calc(var(--spacing-unit) * 4) 0; }

    .philosophy-container { gap: calc(var(--spacing-unit) * 2); }
    .product-grid { grid-template-columns: 1fr; gap: calc(var(--spacing-unit) * 2); }
    .product-card img { height: 250px; } /* Reduce image height */

    .finder-grid { grid-template-columns: repeat(auto-fit, minmax(130px, 1fr)); gap: var(--spacing-unit) * 1.5; }
    .finder-card { min-height: 160px; padding: calc(var(--spacing-unit) * 1.5); }
    .finder-icon-wrapper { width: 55px; height: 55px; margin-bottom: var(--spacing-unit); }
    .finder-icon { font-size: 1.6rem; }
    .finder-card h3 { font-size: 1.1rem; }

    .testimonial-grid { grid-template-columns: 1fr; gap: calc(var(--spacing-unit) * 1.5); }
    .testimonial-card { padding: calc(var(--spacing-unit) * 2); }
    .testimonial-card p { font-size: 1rem; }

    .newsletter-form { flex-direction: column; align-items: stretch; gap: calc(var(--spacing-unit) * 0.8);}
    .newsletter-form input[type="email"] { min-width: auto; width: 100%; }
    .newsletter-form .btn { width: 100%; }

    .footer-grid { grid-template-columns: 1fr; text-align: center; gap: calc(var(--spacing-unit) * 2.5); }
    .footer-about p, .footer-contact p { margin-left: auto; margin-right: auto; }
    .social-icons { justify-content: center; }
    .footer-links ul { padding-left: 0; } /* Remove any potential indent */
    .footer-bottom-container { flex-direction: column; text-align: center; gap: calc(var(--spacing-unit) * 1.5); }
    .payment-methods { justify-content: center; flex-wrap: wrap; } /* Allow payment icons to wrap */
}

```

---

**Description of Design, Approach, and Steps:**

1.  **Overall Goal & Vision:** The aim was to elevate the original design into a premium, calming, and visually engaging experience that evokes the essence of "The Scent." The focus was on creating a sense of tranquility, sophistication, and natural elegance, using the "Wow Effect" principles outlined.

2.  **Color Palette & Typography:**
    *   Implemented the specified `Cormorant Garamond` (headings) and `Montserrat`/`Raleway` (body/accent) fonts via Google Fonts.
    *   Refined the provided color palette slightly for better harmony and sophistication (e.g., deeper slate blue primary, softer mint secondary, muted gold accent). These colors are applied consistently through CSS variables (`:root`).
    *   Used `clamp()` for responsive font sizes, ensuring readability and visual hierarchy across devices.

3.  **Layout & Structure:**
    *   **Hero Section:** Made truly full-height (`100vh`) with a high-quality background image (placeholder used). Added a subtle gradient overlay (`hero-overlay`) for better text contrast and mood. Implemented a subtle zoom animation (`zoomInOut`) on the background and a fade-in/up animation (`fadeInHeroContent`) for the text/CTA. Included a bouncing scroll-down indicator for visual cueing. Typography is large and elegant (`hero-title`, `hero-subtitle`).
    *   **Philosophy Section:** Used an asymmetric CSS grid (`philosophy-container`) for visual interest. Added hover effects to the image (slight scale/rotate) and subtle entrance animations using Intersection Observer. Kept text focused and used italics for emphasis.
    *   **Products Section:** Employed a responsive CSS grid (`product-grid`). Redesigned product cards (`product-card`) with better spacing, fixed image height (`object-fit: cover`), added placeholder prices, subtle hover lift/shadow effects, image zoom on hover, and an overlay "Quick View" button appearing on hover. Product info layout is refined using flexbox.
    *   **Scent Finder Section:** Gave this section a distinct background (`--color-accent-light`). Used a grid (`finder-grid`) for the category cards (`finder-card`). Made cards interactive links. Styled cards with semi-transparent backgrounds, blur effect, redesigned icons within styled wrappers (`finder-icon-wrapper`), and hover effects (background change, transform, icon wrapper style change). Added a clear CTA for the quiz.
    *   **Testimonials Section:** Used a responsive grid (`testimonial-grid`). Styled testimonial cards (`testimonial-card`) with a top accent border, softer shadows, star ratings, semantic `blockquote`/`cite` tags, and an optional subtle background quote icon (`::before`).
    *   **Newsletter Section:** Designed with a distinct background color (`--color-secondary`). Added a decorative icon. Styled the form with pill-shaped, slightly transparent input and a prominent, distinct button style.
    *   **Footer:** Used a darker background (`--color-primary-dark`). Organized content into a responsive grid (`footer-grid`). Styled links with hover effects. Used the logo style for the "About" title. Included social media icons with enhanced hover effects and payment method icons. Added the current year dynamically via JS.
    *   **Whitespace:** Generous padding and margins are used throughout (`section` padding, `gap` in grids, `margin-bottom` on elements) to create a breathable, uncluttered, and premium feel.

4.  **"Wow Effect" Implementation:**
    *   **Imagery:** Although placeholders are used, the CSS styles images for impact (cover fit, subtle hover zoom). The Hero image is central.
    *   **Typography:** Elegant font pairing and careful sizing/weight selection contribute significantly to the premium feel.
    *   **Layout:** Moving beyond simple stacks with grids (asymmetric in Philosophy, flexible in Products/Finder/Testimonials/Footer) creates visual interest. The full-height hero is immediately impactful.
    *   **Micro-interactions:** Subtle hover effects are added to almost all interactive elements (buttons, nav links, product cards, finder cards, social icons) – including transforms (`translateY`, `scale`), shadow changes, and color/background transitions. The sticky header has a smooth transition and blur effect.
    *   **Subtle Animations:** The hero background zoom, hero content fade-in, and the scroll-down indicator add dynamism. A simple fade-in effect using the Intersection Observer API is applied to key section elements as they scroll into view, adding a touch of elegance without being overwhelming.

5.  **Code Quality & Responsiveness:**
    *   Used semantic HTML5.
    *   Employed CSS variables extensively for maintainability.
    *   Organized CSS logically.
    *   Included basic accessibility considerations (ARIA labels, focus states).
    *   Ensured responsiveness using media queries, adjusting layouts, font sizes, and spacing for tablets and mobile devices.
    *   Refined the mobile navigation to be a full-screen overlay with smoother transitions and body scroll prevention (`body.no-scroll`).

This improved version provides a much more polished, unique, and premium foundation that directly addresses the requirements for a "Wow Effect" landing page for "The Scent."  
https://aistudio.google.com/app/prompts?state=%7B%22ids%22:%5B%2210PM7zv_w0EEcZ7USVqyiDHDaKKADlxcM%22%5D,%22action%22:%22open%22,%22userId%22:%22103961307342447084491%22,%22resourceKeys%22:%7B%7D%7D&usp=sharing

---
Here's a breakdown of the thought process to generate the improved landing page for "The Scent":

1.  **Understand the Goal:** The core objective is to create a *visually stunning, unique, premium, calming, and engaging* landing page for "The Scent," incorporating a "Wow Effect." It needs to showcase products, communicate the brand mission (well-being, natural ingredients), and follow a specific structural plan (Hero, Philosophy, Products, Finder, Story, Testimonials, Newsletter, Footer). Key elements like typography, color, imagery, layout, and micro-interactions are emphasized.

2.  **Analyze the Provided Sample:**
    *   **HTML:** It's a well-structured basic layout with semantic sections (header, main, footer, sections with IDs). It uses Google Fonts and Font Awesome. It has a functional mobile menu toggle. The content placeholders match the required sections.
    *   **CSS:** It uses CSS variables (`:root`), basic resets, responsive design principles (media queries), and styles the core elements. It has a basic sticky header and some hover effects. The color palette and typography choices are already defined based on the requirements.
    *   **Weaknesses (from the perspective of "Wow Effect"):** While functional, it's quite standard. Layouts are mostly stacked blocks (except the about section). Animations are minimal (hero text fade-in, subtle zoom). Interactions are basic hovers. It lacks the *unique* visual flair and *premium* feel the prompt asks for.

3.  **Deconstruct the Requirements & Plan:**

    *   **Hero Section:** Needs to be full-screen/large, high-quality image/video, compelling text, CTA. *Plan:* Use `100vh`, a high-res background image (initially, video later if specified), `background-attachment: fixed` for basic parallax, overlay for text contrast, elegant typography (`Cormorant Garamond`), and a clear button. Add subtle animation (fade-in, maybe background zoom).
    *   **Our Philosophy/Mission:** Text + visual. *Plan:* Reuse the sample's two-column layout (`grid`), but enhance it. Add subtle hover effects on the image, ensure good spacing and typography.
    *   **Featured Products:** Visually engaging grid/carousel. Hover effects. *Plan:* Use a CSS grid (`repeat(auto-fit, minmax(...))`) for responsiveness. Style the cards (`product-card`) with rounded corners, subtle shadows, image zoom/opacity change on hover, and a clear link. Keep text minimal and clean.
    *   **Discover Your Scent (Categories):** Unique visual representation (icons, colors, textures). *Plan:* Create a grid for categories (`finder-grid`). Use icons (Font Awesome for now, custom SVGs would be better). Style the cards (`finder-card`) with a distinct background (maybe semi-transparent or using a brand color), hover effects (transform, background change), and evocative icons/text. Use a relevant background color for the *section* itself (like the soft mint green).
    *   **The Art of Aromatherapy (Optional):** Storytelling, global sourcing, etc. *Plan:* This wasn't explicitly in the sample, but the "About" section covers part of it. For a *dedicated* section, I'd consider a more narrative layout, perhaps alternating image/text blocks or using a timeline graphic. *Decision:* Stick to the sample structure for now, enhance the "About" section to carry this weight.
    *   **Testimonials:** Clean presentation. *Plan:* Use a grid layout (`testimonial-grid`). Style cards (`testimonial-card`) with a distinct visual element (like the accent border), clear typography, and perhaps star ratings.
    *   **Join Our Community (Newsletter):** Aesthetically pleasing form. *Plan:* Create a dedicated section with a strong background color (like the primary teal). Style the form for visual appeal – rounded inputs/buttons, good spacing, clear hierarchy.
    *   **Footer:** Standard links, consistent styling. *Plan:* Use a grid (`footer-grid`) for layout. Use a dark background. Style links clearly. Include social icons and possibly payment methods. Ensure consistency with the overall design.

4.  **Implement "Wow" Elements:**

    *   **Typography:** Apply `Cormorant Garamond` to headings (`h1`-`h6`) and `Montserrat`/`Raleway` to body text (`body`, `p`, buttons, nav links) as specified. Ensure appropriate weights and sizes. Use `clamp()` for responsive font sizing.
    *   **Color Palette:** Define the specified colors in `:root` variables and apply them consistently: `--color-primary` (deep teal) for headings, primary buttons, key accents; `--color-secondary` (soft mint) for backgrounds, borders, secondary accents; `--color-accent` (muted gold) for hover states, CTAs, special highlights; `--color-background` (warm off-white) for the body; `--color-text` (dark grey) for body copy.
    *   **Imagery:** Use the provided placeholder URLs. Emphasize the need for *high-quality* actual images in the description. Apply effects like hover opacity changes or subtle scaling.
    *   **Layout:**
        *   *Hero:* Full viewport height.
        *   *About:* Maintain the grid but refine spacing and visual hierarchy.
        *   *Products/Testimonials/Finder:* Use CSS Grid for flexible and responsive layouts (`repeat(auto-fit, minmax(...))`).
        *   *Whitespace:* Ensure generous spacing using `padding`, `margin`, and `gap` properties. Avoid clutter.
        *   *Asymmetry/Overlapping:* While not heavily implemented in *this* iteration (to keep it manageable), the prompt mentions it. This could be achieved with absolute positioning or negative margins, but adds complexity. *Decision:* Keep layouts clean but well-spaced for this version. The two-column "About" section provides some asymmetry.
    *   **Micro-interactions:**
        *   *Buttons:* Add `transform: translateY(-2px)` on hover.
        *   *Nav Links:* Add underline hover effect.
        *   *Product Cards:* Add `transform: translateY(-5px)` and `box-shadow` change on hover. Image opacity change.
        *   *Finder Cards:* Add `transform: translateY(-5px)` and background change on hover.
        *   *Sticky Header:* Implement smooth transition.
        *   *Hero Animation:* Subtle zoom on background, fade-in on content.
        *   *Scroll Animations:* Mentioned as a *further enhancement* using JS, not implemented directly in the CSS/HTML to keep it focused on the structure and base styling.

5.  **Refine and Structure CSS:**
    *   Use CSS variables extensively for maintainability.
    *   Organize CSS logically: Base styles, helpers (container, buttons), component styles (header, hero, about, products, etc.), responsive styles (media queries).
    *   Use comments to explain sections.
    *   Apply `box-sizing: border-box`.
    *   Add basic resets.
    *   Ensure responsiveness using media queries, targeting common breakpoints (e.g., 992px for tablets, 576px for mobile). Adjust layouts, font sizes, and spacing accordingly. Handle the mobile navigation toggle and display.

6.  **Refine HTML:**
    *   Use semantic HTML5 tags (`header`, `nav`, `main`, `section`, `footer`, `aside` if needed).
    *   Use appropriate ARIA attributes (e.g., `aria-label` for icon buttons, potentially `aria-controls`/`aria-expanded` for mobile nav toggle, though the simple JS handles it visually).
    *   Ensure logical content flow.
    *   Add IDs to sections for anchor links (`#hero`, `#about`, etc.).
    *   Add classes strategically for styling.

7.  **JavaScript:** Keep it minimal as requested by the sample.
    *   Implement the mobile menu toggle logic.
    *   Add the simple sticky header class toggle based on scroll position.

8.  **Review and Describe:**
    *   Double-check the code against the requirements. Does it look premium? Calming? Engaging? Does it incorporate the planned elements?
    *   Write the description: Explain the overall approach, detail the specific choices made for each section (Hero, Products, Finder etc.), highlight how the "Wow" elements (typography, color, layout, interactions) were integrated, and mention potential further enhancements. Explain the *why* behind the design decisions.

**(Self-Correction during the process):**

*   *Initial thought:* Maybe use complex background gradients or patterns. *Correction:* The prompt emphasizes "calming" and "natural." Stick to the defined color palette derived from nature and high-quality imagery. Keep backgrounds cleaner unless a texture explicitly adds to the natural feel (like a subtle paper texture, but decided against for simplicity here).
*   *Initial thought:* Add lots of complex animations. *Correction:* Over-animation can be distracting and detrimental to a "calming" feel. Focus on *subtle* micro-interactions (hovers, smooth transitions) and maybe one or two key entrance animations (like the hero). Suggest more advanced animations (scroll-based) as further enhancements.
*   *Initial thought:* Make the "Finder" section super interactive with JS. *Correction:* Keep the initial implementation simple (HTML/CSS grid with hover states) and suggest the full interactive quiz as a next step. This fits the scope of creating the *landing page structure and style*.
*   *Ensure CSS Naming:* Use consistent and understandable class names (e.g., `product-card`, `finder-card`, `testimonial-card`).
*   *Accessibility:* Add `aria-label` attributes to icon-only buttons. Ensure sufficient color contrast (though the chosen palette seems generally okay, this would need formal checking). Use semantic HTML.

By following these steps, combining the structural requirements with the aesthetic goals and "Wow" factors, the resulting HTML and CSS aim to deliver a significantly improved and more premium landing page experience compared to the initial sample.

---
Now you will craft a visually stunning and unique landing page for "The Scent." You will aim for a premium, calming, and engaging feel, incorporating the "Wow Effect" through layout, imagery, and subtle details, while ensuring it reflects the company's mission and showcases the products.

Based on the requirements, use the sample HTML page below to create your improved HTML code. Here is your plan / approach to acheive the goal of a "Wow Effect":

1.  **Hero Section:** Full-screen or large hero image/video background with a compelling headline, short mission statement, and a clear Call-to-Action (CTA). We'll use high-quality imagery and elegant typography.
2.  **Our Philosophy/Mission:** A section explaining the brand's focus on mental/physical well-being and quality ingredients, perhaps pairing text with a relevant visual.
3.  **Featured Products:** A visually engaging grid or carousel showcasing the provided essential oil and soap images with minimal, clean text. Hover effects can add interactivity.
4.  **Discover Your Scent (Categories):** A unique visual representation of scent categories (Relaxation, Energy, etc.), potentially using icons, colors, and background textures that evoke the mood. This leads users towards exploration.
5.  **The Art of Aromatherapy (Optional Storytelling):** A section detailing the global sourcing, creative formulation process, and the relevance of aromatherapy today, reinforcing the premium aspect.
6.  **Testimonials:** Cleanly presented customer feedback to build trust.
7.  **Join Our Community (Newsletter):** An aesthetically pleasing signup form integrated into the page design.
8.  **Footer:** Standard links, contact information, social media icons, and copyright, styled consistently.

**Key "Wow" Elements:**

*   **Typography:** Using `Cormorant Garamond` for headings and `Montserrat` or `Raleway` for body text creates an elegant contrast.
*   **Color Palette:** We'll use a sophisticated palette derived from nature – deep greens, earthy tones, soft neutrals, maybe a touch of gold or copper for accents.
*   **Imagery:** High-resolution, evocative images are crucial.
*   **Layout:** Moving beyond simple stacked blocks. Using asymmetric layouts, overlapping elements (subtly), and generous whitespace.
*   **Micro-interactions:** Subtle hover effects, smooth transitions, maybe parallax scrolling on the hero image.

---

Here is the HTML (`index.html`) and CSS (`style.css`) code for the sample landing page. Use them as your reference only to create your own improved version based on the above requirements. After creating, please describe your design and explain your approach and steps taken.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Scent - Premium Aromatherapy & Natural Well-being</title>
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;600;700&family=Montserrat:wght@300;400;500&family=Raleway:wght@400;500;600&display=swap" rel="stylesheet">
    <!-- Font Awesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" integrity="sha512-9usAa10IRO0HhonpyAIVpjrylPvoDwiPUiKdWk5t3PyolY1cOd4DSE0Ga+ri4AuTroPR5aQvXU9xC6qOPnzFeg==" crossorigin="anonymous" referrerpolicy="no-referrer" />
    <!-- Link to CSS -->
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Header -->
    <header class="main-header">
        <div class="container header-container">
            <div class="logo">
                <a href="#">The Scent</a>
                <span>AROMATHERAPY</span>
            </div>
            <nav class="main-nav">
                <ul>
                    <li><a href="#hero">Home</a></li>
                    <li><a href="#products">Shop</a></li>
                    <li><a href="#finder">Scent Finder</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
            <div class="header-icons">
                <a href="#" aria-label="Search"><i class="fas fa-search"></i></a>
                <a href="#" aria-label="Account"><i class="fas fa-user"></i></a>
                <a href="#" aria-label="Cart"><i class="fas fa-shopping-bag"></i></a>
            </div>
             <button class="mobile-nav-toggle" aria-label="Toggle navigation">
                <i class="fas fa-bars"></i>
            </button>
        </div>
         <!-- Mobile Menu (hidden by default) -->
        <nav class="mobile-nav">
            <ul>
                <li><a href="#hero">Home</a></li>
                <li><a href="#products">Shop</a></li>
                <li><a href="#finder">Scent Finder</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
                 <li><a href="#">Search</a></li>
                <li><a href="#">Account</a></li>
                <li><a href="#">Cart</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <!-- Hero Section -->
        <section id="hero" class="hero-section">
            <div class="hero-background">
                <!-- Background image set in CSS -->
            </div>
            <div class="container hero-content">
                <h1>Find Your Moment of Calm</h1>
                <p>Elevate your well-being with our premium, natural aromatherapy products, crafted to restore balance and peace.</p>
                <a href="#products" class="btn btn-primary">Explore Our Collections</a>
            </div>
        </section>

        <!-- About/Mission Section -->
        <section id="about" class="about-section">
            <div class="container about-container">
                <div class="about-image">
                     <img src="https://raw.githubusercontent.com/nordeim/The-Scent/refs/heads/main/images/scent6.jpg" alt="Natural ingredients used in The Scent products">
                </div>
                <div class="about-text">
                    <h2>Rooted in Nature, Crafted with Care</h2>
                    <p>At The Scent, we believe in the power of nature to nurture mental and physical health. We meticulously source high-quality raw materials from around the globe, creating unique and harmonious aromatherapy blends. Our passion lies in crafting balanced, well-rounded products designed to help you navigate the stresses of modern life.</p>
                    <a href="#" class="btn btn-secondary">Learn Our Story</a>
                </div>
            </div>
        </section>

        <!-- Featured Products Section -->
        <section id="products" class="products-section">
            <div class="container">
                <h2>Featured Collections</h2>
                <div class="product-grid">
                    <!-- Product 1: Essential Oil -->
                    <div class="product-card">
                        <img src="https://raw.githubusercontent.com/nordeim/The-Scent/refs/heads/main/images/scent2.jpg" alt="Essential Oil Blend 1">
                        <div class="product-info">
                            <h3>Serenity Blend Oil</h3>
                            <p>Calming Lavender & Chamomile</p>
                            <a href="#" class="product-link">View Product</a>
                        </div>
                    </div>
                    <!-- Product 2: Soap -->
                    <div class="product-card">
                        <img src="https://raw.githubusercontent.com/nordeim/The-Scent/refs/heads/main/images/soap4.jpg" alt="Natural Soap 1">
                        <div class="product-info">
                            <h3>Citrus Burst Soap</h3>
                            <p>Energizing Lemon & Orange Peel</p>
                            <a href="#" class="product-link">View Product</a>
                        </div>
                    </div>
                    <!-- Product 3: Essential Oil -->
                     <div class="product-card">
                        <img src="https://raw.githubusercontent.com/nordeim/The-Scent/refs/heads/main/images/scent4.jpg" alt="Essential Oil Blend 2">
                        <div class="product-info">
                            <h3>Focus Flow Oil</h3>
                            <p>Invigorating Rosemary & Mint</p>
                            <a href="#" class="product-link">View Product</a>
                        </div>
                    </div>
                     <!-- Product 4: Soap -->
                    <div class="product-card">
                        <img src="https://raw.githubusercontent.com/nordeim/The-Scent/refs/heads/main/images/soap6.jpg" alt="Natural Soap 2">
                         <div class="product-info">
                            <h3>Woodland Retreat Soap</h3>
                            <p>Grounding Cedarwood & Pine</p>
                            <a href="#" class="product-link">View Product</a>
                        </div>
                    </div>
                </div>
                 <div class="view-all-cta">
                     <a href="#" class="btn btn-primary">Shop All Products</a>
                 </div>
            </div>
        </section>

        <!-- Scent Finder Section -->
        <section id="finder" class="finder-section">
            <div class="container">
                <h2>Discover Your Perfect Scent</h2>
                <p class="finder-subtitle">Tailor your aromatherapy experience to your mood and needs.</p>
                <div class="finder-grid">
                    <div class="finder-card">
                        <i class="fas fa-leaf finder-icon"></i>
                        <h3>Relaxation</h3>
                        <p>Calming scents to help you unwind.</p>
                    </div>
                    <div class="finder-card">
                        <i class="fas fa-bolt finder-icon"></i>
                        <h3>Energy</h3>
                        <p>Invigorating scents to boost vitality.</p>
                    </div>
                    <div class="finder-card">
                        <i class="fas fa-brain finder-icon"></i>
                        <h3>Focus</h3>
                        <p>Clarifying scents for concentration.</p>
                    </div>
                     <div class="finder-card">
                        <i class="fas fa-moon finder-icon"></i>
                        <h3>Sleep</h3>
                        <p>Soothing scents for restful nights.</p>
                    </div>
                    <div class="finder-card">
                         <i class="fas fa-balance-scale finder-icon"></i>
                        <h3>Balance</h3>
                        <p>Harmonizing scents to center your mind.</p>
                    </div>
                </div>
                <div class="finder-cta">
                    <a href="#" class="btn btn-secondary">Take the Full Scent Quiz</a>
                </div>
            </div>
        </section>

         <!-- Testimonials Section -->
        <section id="testimonials" class="testimonials-section">
            <div class="container">
                <h2>What Our Community Says</h2>
                 <div class="testimonial-grid">
                    <div class="testimonial-card">
                        <p>"The Lavender Essential Oil transformed my bedtime routine. The calming aroma helps me unwind like never before. Pure quality!"</p>
                        <span class="testimonial-author">- Sarah L., Los Angeles</span>
                         <div class="testimonial-rating">★★★★★</div>
                    </div>
                     <div class="testimonial-card">
                        <p>"I was skeptical, but the Focus Blend oil genuinely improved my concentration while working from home. It's subtle but effective."</p>
                        <span class="testimonial-author">- Michael T., Chicago</span>
                        <div class="testimonial-rating">★★★★★</div>
                    </div>
                    <div class="testimonial-card">
                         <p>"These handcrafted soaps are amazing! They smell divine, helped clear my sensitive skin, and feel so much better than store-bought."</p>
                         <span class="testimonial-author">- Emma R., Seattle</span>
                         <div class="testimonial-rating">★★★★★</div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Newsletter Section -->
        <section id="newsletter" class="newsletter-section">
            <div class="container newsletter-container">
                 <h2>Join Our Community</h2>
                 <p>Subscribe for exclusive offers, aromatherapy tips, and early access to new products.</p>
                <form class="newsletter-form">
                    <input type="email" placeholder="Your email address" required>
                    <button type="submit" class="btn btn-primary">Subscribe</button>
                </form>
                 <p class="newsletter-consent">By subscribing, you agree to our Privacy Policy.</p>
            </div>
        </section>

    </main>

    <!-- Footer -->
    <footer id="contact" class="main-footer">
        <div class="container footer-grid">
            <div class="footer-about">
                <h3>About The Scent</h3>
                <p>Creating premium aromatherapy products to enhance mental and physical well-being through the power of scent.</p>
                 <div class="social-icons">
                    <a href="#" aria-label="Facebook"><i class="fab fa-facebook-f"></i></a>
                    <a href="#" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
                    <a href="#" aria-label="Twitter"><i class="fab fa-twitter"></i></a>
                    <a href="#" aria-label="Pinterest"><i class="fab fa-pinterest"></i></a>
                </div>
            </div>
             <div class="footer-links">
                <h3>Shop</h3>
                <ul>
                    <li><a href="#">Essential Oils</a></li>
                    <li><a href="#">Natural Soaps</a></li>
                    <li><a href="#">Gift Sets</a></li>
                    <li><a href="#">New Arrivals</a></li>
                    <li><a href="#">Bestsellers</a></li>
                </ul>
            </div>
            <div class="footer-links">
                <h3>Help</h3>
                 <ul>
                    <li><a href="#">Contact Us</a></li>
                    <li><a href="#">FAQs</a></li>
                    <li><a href="#">Shipping & Returns</a></li>
                    <li><a href="#">Track Your Order</a></li>
                    <li><a href="#">Privacy Policy</a></li>
                </ul>
            </div>
             <div class="footer-contact">
                 <h3>Contact Us</h3>
                <p><i class="fas fa-map-marker-alt"></i> 123 Aromatherapy Lane, Wellness City, WB 12345</p>
                <p><i class="fas fa-phone"></i> +1 (555) 123-4567</p>
                <p><i class="fas fa-envelope"></i> hello@thescent.com</p>
            </div>
        </div>
        <div class="footer-bottom">
            <div class="container">
                <p>&copy; 2025 The Scent. All rights reserved.</p>
                <!-- Add payment method icons if needed -->
                 <div class="payment-methods">
                     <span>Accepted Payments:</span>
                    <i class="fab fa-cc-visa"></i>
                    <i class="fab fa-cc-mastercard"></i>
                    <i class="fab fa-cc-paypal"></i>
                    <i class="fab fa-cc-amex"></i>
                 </div>
            </div>
        </div>
    </footer>

    <script>
        // Basic Mobile Menu Toggle
        const toggleButton = document.querySelector('.mobile-nav-toggle');
        const mobileNav = document.querySelector('.mobile-nav');
        const mainHeader = document.querySelector('.main-header');

        if (toggleButton && mobileNav && mainHeader) {
            toggleButton.addEventListener('click', () => {
                mobileNav.classList.toggle('active');
                mainHeader.classList.toggle('mobile-menu-active'); // Add class to header
                 // Change icon
                const icon = toggleButton.querySelector('i');
                if (mobileNav.classList.contains('active')) {
                    icon.classList.remove('fa-bars');
                    icon.classList.add('fa-times');
                } else {
                    icon.classList.remove('fa-times');
                    icon.classList.add('fa-bars');
                }
            });
             // Close menu when a link is clicked
            mobileNav.querySelectorAll('a').forEach(link => {
                link.addEventListener('click', () => {
                     mobileNav.classList.remove('active');
                     mainHeader.classList.remove('mobile-menu-active');
                      const icon = toggleButton.querySelector('i');
                        icon.classList.remove('fa-times');
                        icon.classList.add('fa-bars');
                });
            });
        }

         // Simple sticky header effect
        window.addEventListener('scroll', () => {
            if (window.scrollY > 50) {
                 mainHeader.classList.add('sticky');
            } else {
                mainHeader.classList.remove('sticky');
             }
        });

    </script>

</body>
</html>
```

**style.css:**

```css
/* --- Base Styles & Variables --- */
:root {
    --font-heading: 'Cormorant Garamond', serif;
    --font-body: 'Montserrat', sans-serif;
    --font-accent: 'Raleway', sans-serif;

    --color-primary: #1A4D5A; /* Deep Teal */
    --color-secondary: #A0C1B1; /* Soft Mint Green */
    --color-accent: #D4A76A; /* Muted Gold/Ochre */
    --color-background: #F8F5F2; /* Warm Off-White */
    --color-text: #333333; /* Dark Grey */
    --color-text-light: #FFFFFF;
    --color-border: #e0e0e0;

    --container-width: 1200px;
    --spacing-unit: 1rem; /* Approx 16px */

    --transition-speed: 0.3s;
}

*, *::before, *::after {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

html {
    scroll-behavior: smooth;
    font-size: 100%; /* Base font size (usually 16px) */
}

body {
    font-family: var(--font-body);
    color: var(--color-text);
    background-color: var(--color-background);
    line-height: 1.7;
    overflow-x: hidden; /* Prevent horizontal scroll */
}

h1, h2, h3, h4, h5, h6 {
    font-family: var(--font-heading);
    font-weight: 600;
    color: var(--color-primary);
    margin-bottom: calc(var(--spacing-unit) * 1);
    line-height: 1.2;
}

h1 { font-size: clamp(2.5rem, 5vw, 4rem); }
h2 { font-size: clamp(1.8rem, 4vw, 2.8rem); }
h3 { font-size: clamp(1.3rem, 3vw, 1.8rem); }

p {
    margin-bottom: calc(var(--spacing-unit) * 1);
    max-width: 70ch; /* Improve readability */
}

a {
    color: var(--color-primary);
    text-decoration: none;
    transition: color var(--transition-speed) ease;
}

a:hover, a:focus {
    color: var(--color-accent);
}

img {
    max-width: 100%;
    height: auto;
    display: block;
}

ul {
    list-style: none;
}

.container {
    width: 90%;
    max-width: var(--container-width);
    margin: 0 auto;
    padding: 0 var(--spacing-unit);
}

/* --- Buttons --- */
.btn {
    display: inline-block;
    font-family: var(--font-accent);
    font-weight: 500;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    padding: calc(var(--spacing-unit) * 0.8) calc(var(--spacing-unit) * 2);
    border-radius: 50px; /* Pill shape */
    cursor: pointer;
    transition: background-color var(--transition-speed) ease, color var(--transition-speed) ease, transform var(--transition-speed) ease;
    border: 2px solid transparent;
}

.btn-primary {
    background-color: var(--color-primary);
    color: var(--color-text-light);
    border-color: var(--color-primary);
}

.btn-primary:hover, .btn-primary:focus {
    background-color: var(--color-accent);
    border-color: var(--color-accent);
    color: var(--color-text-light);
    transform: translateY(-2px);
}

.btn-secondary {
    background-color: transparent;
    color: var(--color-primary);
    border-color: var(--color-primary);
}

.btn-secondary:hover, .btn-secondary:focus {
    background-color: var(--color-primary);
    color: var(--color-text-light);
     transform: translateY(-2px);
}

/* --- Header --- */
.main-header {
    position: absolute; /* Overlay on hero */
    top: 0;
    left: 0;
    width: 100%;
    z-index: 1000;
    padding: calc(var(--spacing-unit) * 1.5) 0;
    background: transparent;
    transition: background-color var(--transition-speed) ease, box-shadow var(--transition-speed) ease, padding var(--transition-speed) ease;
}
.main-header.sticky {
     position: fixed;
     background-color: rgba(255, 255, 255, 0.95); /* Slightly transparent white */
     box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
     padding: calc(var(--spacing-unit) * 0.8) 0;
}
.main-header.sticky .logo a,
.main-header.sticky .main-nav a,
.main-header.sticky .header-icons a,
.main-header.sticky .mobile-nav-toggle {
    color: var(--color-primary);
}
.main-header.sticky .logo span {
    color: var(--color-text);
}
.main-header.sticky .main-nav a:hover,
.main-header.sticky .header-icons a:hover {
    color: var(--color-accent);
}

.header-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.logo a {
    font-family: var(--font-heading);
    font-size: 1.8rem;
    font-weight: 700;
    color: var(--color-text-light); /* White for hero overlay */
    text-transform: uppercase;
    letter-spacing: 1px;
}
.logo span {
    display: block;
    font-family: var(--font-accent);
    font-size: 0.6rem;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--color-text-light); /* White for hero overlay */
    margin-top: -5px;
    opacity: 0.8;
}


.main-nav ul {
    display: flex;
    gap: calc(var(--spacing-unit) * 2);
}

.main-nav a {
    font-family: var(--font-accent);
    font-weight: 500;
    color: var(--color-text-light); /* White for hero overlay */
    text-transform: uppercase;
    letter-spacing: 1px;
    padding: 5px 0;
    position: relative;
}
/* Underline effect */
.main-nav a::after {
    content: '';
    position: absolute;
    width: 0;
    height: 2px;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
    background-color: var(--color-accent);
    transition: width var(--transition-speed) ease;
}
.main-nav a:hover::after, .main-nav a:focus::after {
    width: 100%;
}


.header-icons {
    display: flex;
    gap: calc(var(--spacing-unit) * 1.5);
}

.header-icons a {
    color: var(--color-text-light); /* White for hero overlay */
    font-size: 1.2rem;
}

.mobile-nav-toggle {
    display: none; /* Hidden on desktop */
    background: none;
    border: none;
    color: var(--color-text-light); /* White for hero overlay */
    font-size: 1.5rem;
    cursor: pointer;
    z-index: 1001; /* Above mobile nav */
}

.mobile-nav {
    display: none; /* Hidden by default */
    position: absolute;
    top: 100%; /* Position below header */
    left: 0;
    width: 100%;
    background-color: rgba(255, 255, 255, 0.98); /* Match sticky header */
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
    padding: var(--spacing-unit);
    max-height: 0;
    overflow: hidden;
     transition: max-height 0.5s ease-out;
}
.mobile-nav.active {
     display: block; /* Show when active */
     max-height: 500px; /* Adjust as needed */
}
.main-header.mobile-menu-active {
     background-color: rgba(255, 255, 255, 0.98); /* Ensure bg when mobile menu is open */
}
.main-header.mobile-menu-active .logo a,
.main-header.mobile-menu-active .logo span,
.main-header.mobile-menu-active .mobile-nav-toggle {
    color: var(--color-primary); /* Darken elements when mobile menu is open */
}


.mobile-nav ul {
    display: flex;
    flex-direction: column;
    gap: var(--spacing-unit);
}

.mobile-nav a {
    display: block;
    padding: calc(var(--spacing-unit) * 0.5);
    color: var(--color-primary);
    font-family: var(--font-accent);
    text-transform: uppercase;
    text-align: center;
    font-size: 1.1rem;
    transition: background-color var(--transition-speed) ease;
}
.mobile-nav a:hover, .mobile-nav a:focus {
     background-color: var(--color-secondary);
     color: var(--color-primary);
}


/* --- Hero Section --- */
.hero-section {
    position: relative;
    height: 100vh; /* Full viewport height */
    min-height: 600px; /* Minimum height */
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    overflow: hidden; /* Ensure pseudo-elements don't overflow */
    color: var(--color-text-light);
}

.hero-background {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-image: url('https://raw.githubusercontent.com/nordeim/The-Scent/refs/heads/main/images/scent5.jpg'); /* Replace with your best hero image */
    background-size: cover;
    background-position: center center;
    background-attachment: fixed; /* Parallax effect */
    z-index: -2;
    animation: zoomInOut 25s infinite alternate ease-in-out; /* Subtle zoom */
}

/* Dark overlay for text contrast */
.hero-section::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.4); /* Adjust darkness */
    z-index: -1;
}

.hero-content {
    position: relative; /* Ensure content is above overlay */
    z-index: 1;
    max-width: 800px;
    animation: fadeIn 1.5s ease-out;
}

.hero-content h1 {
    color: var(--color-text-light);
    font-weight: 700;
    margin-bottom: calc(var(--spacing-unit) * 1);
}

.hero-content p {
    font-size: 1.2rem;
    margin-bottom: calc(var(--spacing-unit) * 2);
    opacity: 0.9;
     max-width: 60ch;
     margin-left: auto;
     margin-right: auto;
}

/* Animations */
@keyframes fadeIn {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
}

@keyframes zoomInOut {
     from { transform: scale(1); }
    to { transform: scale(1.05); }
}

/* --- Generic Section Styling --- */
section {
    padding: calc(var(--spacing-unit) * 5) 0;
}
section:nth-child(odd) { /* Alternate background for visual separation */
    background-color: #fff; /* Slightly different from body bg */
}
section h2 {
    text-align: center;
    margin-bottom: calc(var(--spacing-unit) * 3);
}

/* --- About Section --- */
.about-section {
    background-color: #fff; /* White background */
}
.about-container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: calc(var(--spacing-unit) * 4);
    align-items: center;
}
.about-image img {
    border-radius: 8px;
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
    transition: transform var(--transition-speed) ease;
}
.about-image img:hover {
    transform: scale(1.03);
}
.about-text h2 {
    text-align: left;
}
.about-text p {
    margin-bottom: calc(var(--spacing-unit) * 2);
}

/* --- Products Section --- */
.product-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: calc(var(--spacing-unit) * 2.5);
}
.product-card {
    background-color: #fff;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.05);
    transition: transform var(--transition-speed) ease, box-shadow var(--transition-speed) ease;
    position: relative;
}
.product-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 25px rgba(0, 0, 0, 0.1);
}
.product-card img {
    width: 100%;
    height: 250px; /* Fixed height */
    object-fit: cover; /* Cover the area */
    transition: opacity var(--transition-speed) ease;
}
.product-card:hover img {
    opacity: 0.85;
}
.product-info {
    padding: calc(var(--spacing-unit) * 1.5);
    text-align: center;
}
.product-info h3 {
    margin-bottom: calc(var(--spacing-unit) * 0.5);
    font-size: 1.3rem;
}
.product-info p {
    font-size: 0.9rem;
    color: #666;
    margin-bottom: calc(var(--spacing-unit) * 1);
}
.product-link {
    font-family: var(--font-accent);
    font-weight: 500;
    color: var(--color-accent);
    text-transform: uppercase;
    font-size: 0.85rem;
    letter-spacing: 0.5px;
    position: relative;
     padding-bottom: 3px;
}
.product-link::after {
    content: '';
    position: absolute;
    width: 0;
    height: 1px;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
    background-color: var(--color-accent);
    transition: width var(--transition-speed) ease;
}
.product-card:hover .product-link::after {
    width: 50%;
}
.view-all-cta {
    text-align: center;
    margin-top: calc(var(--spacing-unit) * 3);
}


/* --- Scent Finder Section --- */
.finder-section {
    background-color: var(--color-secondary); /* Use the soft green */
    color: var(--color-primary); /* Dark text on light bg */
}
.finder-section h2 {
     color: var(--color-primary);
}
.finder-subtitle {
     text-align: center;
     margin-top: calc(var(--spacing-unit) * -2); /* Pull up closer to title */
     margin-bottom: calc(var(--spacing-unit) * 3);
     opacity: 0.9;
}

.finder-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: calc(var(--spacing-unit) * 2);
}
.finder-card {
    background-color: rgba(255, 255, 255, 0.5); /* Semi-transparent white */
    padding: calc(var(--spacing-unit) * 2) calc(var(--spacing-unit) * 1.5);
    border-radius: 8px;
    text-align: center;
    transition: background-color var(--transition-speed) ease, transform var(--transition-speed) ease;
    cursor: pointer;
}
.finder-card:hover {
    background-color: rgba(255, 255, 255, 0.8);
    transform: translateY(-5px);
}
.finder-icon {
    font-size: 2.5rem;
    color: var(--color-primary);
    margin-bottom: var(--spacing-unit);
    display: block;
}
.finder-card h3 {
    font-size: 1.2rem;
     margin-bottom: calc(var(--spacing-unit) * 0.5);
}
.finder-card p {
     font-size: 0.9rem;
     line-height: 1.5;
     color: var(--color-text);
     margin-bottom: 0;
}
.finder-cta {
    text-align: center;
    margin-top: calc(var(--spacing-unit) * 3);
}
.finder-cta .btn-secondary {
     border-color: var(--color-primary); /* Ensure border matches text color */
}
.finder-cta .btn-secondary:hover {
    background-color: var(--color-primary);
    color: var(--color-text-light);
}

/* --- Testimonials Section --- */
.testimonials-section {
    background-color: #fff;
}
.testimonial-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: calc(var(--spacing-unit) * 2);
}
.testimonial-card {
    background-color: var(--color-background); /* Use the warm off-white */
    padding: calc(var(--spacing-unit) * 2);
    border-radius: 8px;
    border-left: 5px solid var(--color-secondary); /* Accent border */
    box-shadow: 0 4px 10px rgba(0,0,0,0.03);
}
.testimonial-card p {
    font-style: italic;
    margin-bottom: var(--spacing-unit);
    color: #555;
}
.testimonial-author {
    display: block;
    font-weight: 500;
    color: var(--color-primary);
    margin-bottom: calc(var(--spacing-unit) * 0.5);
}
.testimonial-rating {
    color: var(--color-accent);
    font-size: 1.1rem;
}

/* --- Newsletter Section --- */
.newsletter-section {
     background-color: var(--color-primary);
     color: var(--color-text-light);
     padding: calc(var(--spacing-unit) * 4) 0;
}
.newsletter-section h2 {
    color: var(--color-text-light);
}
.newsletter-container {
     text-align: center;
     max-width: 700px;
}
.newsletter-container p {
    opacity: 0.9;
    margin-bottom: calc(var(--spacing-unit) * 1.5);
}
.newsletter-form {
    display: flex;
    justify-content: center;
    gap: var(--spacing-unit);
    margin-bottom: var(--spacing-unit);
    flex-wrap: wrap; /* Wrap on smaller screens */
}
.newsletter-form input[type="email"] {
    padding: calc(var(--spacing-unit) * 0.8);
    border: 1px solid var(--color-secondary);
    border-radius: 50px;
    font-family: var(--font-body);
    min-width: 300px;
    flex-grow: 1; /* Take available space */
}
.newsletter-form .btn {
    background-color: var(--color-accent);
    color: var(--color-primary);
    border-color: var(--color-accent);
}
.newsletter-form .btn:hover {
    background-color: var(--color-secondary);
    border-color: var(--color-secondary);
    color: var(--color-primary);
}
.newsletter-consent {
    font-size: 0.8rem;
    opacity: 0.7;
    margin-bottom: 0;
}
.newsletter-consent a {
    color: var(--color-secondary);
    text-decoration: underline;
}
.newsletter-consent a:hover {
    color: var(--color-text-light);
}

/* --- Footer --- */
.main-footer {
    background-color: #2f3d41; /* Darker shade */
    color: #ccc;
    padding-top: calc(var(--spacing-unit) * 4);
    font-size: 0.9rem;
}
.footer-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: calc(var(--spacing-unit) * 3);
    margin-bottom: calc(var(--spacing-unit) * 3);
}
.footer-about h3, .footer-links h3, .footer-contact h3 {
    font-family: var(--font-accent);
    color: var(--color-text-light);
    font-weight: 600;
    margin-bottom: calc(var(--spacing-unit) * 1.2);
    font-size: 1.1rem;
}
.footer-about p {
    line-height: 1.6;
    margin-bottom: var(--spacing-unit);
}
.social-icons {
    display: flex;
    gap: var(--spacing-unit);
}
.social-icons a {
    color: #ccc;
    font-size: 1.2rem;
    transition: color var(--transition-speed) ease, transform var(--transition-speed) ease;
}
.social-icons a:hover {
    color: var(--color-accent);
    transform: scale(1.1);
}

.footer-links ul li {
    margin-bottom: calc(var(--spacing-unit) * 0.5);
}
.footer-links a {
    color: #ccc;
}
.footer-links a:hover {
    color: var(--color-text-light);
    text-decoration: underline;
}
.footer-contact p {
    margin-bottom: calc(var(--spacing-unit) * 0.6);
    display: flex;
    align-items: center;
    gap: calc(var(--spacing-unit) * 0.5);
}
.footer-contact i {
    color: var(--color-secondary);
    width: 16px; /* Align icons */
    text-align: center;
}

.footer-bottom {
    background-color: #222b2e; /* Even darker */
    padding: calc(var(--spacing-unit) * 1.5) 0;
    margin-top: calc(var(--spacing-unit) * 2);
}
.footer-bottom .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap; /* Wrap on small screens */
    gap: var(--spacing-unit);
    font-size: 0.85rem;
}
.payment-methods {
    display: flex;
    align-items: center;
    gap: calc(var(--spacing-unit) * 0.8);
}
.payment-methods span {
     margin-right: calc(var(--spacing-unit) * 0.5);
}
.payment-methods i {
    font-size: 1.8rem;
    color: #aaa;
}


/* --- Responsive Design --- */

/* Tablets and smaller desktops */
@media (max-width: 992px) {
    .header-container {
        padding: 0 calc(var(--spacing-unit) * 1.5); /* More padding on smaller screens */
    }
     .main-nav {
        display: none; /* Hide desktop nav */
    }
    .header-icons {
        display: none; /* Hide icons or move to mobile menu */
    }
    .mobile-nav-toggle {
        display: block; /* Show hamburger */
    }
    .about-container {
        grid-template-columns: 1fr; /* Stack elements */
        text-align: center;
    }
     .about-image {
         margin-bottom: calc(var(--spacing-unit) * 2);
         order: -1; /* Move image above text */
     }
    .about-text h2 {
         text-align: center;
    }
    .footer-grid {
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); /* Adjust columns */
    }
}

/* Mobile phones */
@media (max-width: 576px) {
    h1 { font-size: 2rem; }
    h2 { font-size: 1.6rem; }
    h3 { font-size: 1.2rem; }

    .hero-section {
        min-height: 500px;
    }
     .hero-content p {
        font-size: 1rem;
    }
     .btn {
         padding: calc(var(--spacing-unit) * 0.7) calc(var(--spacing-unit) * 1.5);
         font-size: 0.9rem;
    }

     section {
        padding: calc(var(--spacing-unit) * 3) 0;
    }
     section h2 {
        margin-bottom: calc(var(--spacing-unit) * 2);
    }

    .product-grid {
        grid-template-columns: 1fr; /* Single column */
        gap: calc(var(--spacing-unit) * 1.5);
    }
     .finder-grid {
        grid-template-columns: repeat(auto-fit, minmax(140px, 1fr)); /* Allow smaller cards */
        gap: var(--spacing-unit);
    }
    .finder-card {
        padding: calc(var(--spacing-unit) * 1.5) var(--spacing-unit);
    }
     .testimonial-grid {
         grid-template-columns: 1fr;
     }
    .newsletter-form {
        flex-direction: column; /* Stack form elements */
        align-items: stretch; /* Full width */
    }
     .newsletter-form input[type="email"] {
         min-width: auto;
         width: 100%;
    }
    .newsletter-form .btn {
         width: 100%;
    }

    .footer-grid {
        grid-template-columns: 1fr; /* Single column */
        text-align: center;
    }
     .footer-about p, .footer-contact p {
         justify-content: center;
     }
     .social-icons {
        justify-content: center;
        margin-top: var(--spacing-unit);
    }
    .footer-bottom .container {
        flex-direction: column;
        text-align: center;
    }
    .payment-methods {
        margin-top: var(--spacing-unit);
    }

}
```

**Further Enhancements for "Wow":**

1.  **Animations on Scroll:** Use a small JavaScript library (like AOS - Animate On Scroll or Intersection Observer API) to make elements fade or slide in as the user scrolls down the page.
2.  **Interactive Scent Finder:** Develop the "Take the Full Scent Quiz" button to lead to an actual interactive quiz page.
3.  **Hero Video:** Replace the hero background image with a calming, high-quality background video loop (nature, flowing liquids, etc.). Ensure it's optimized for web use.
4.  **Parallax Depth:** Implement more advanced parallax effects where different layers move at different speeds for a greater sense of depth.
5.  **Product Image Carousel:** If you have many featured products, use a subtle carousel/slider instead of a static grid.
6.  **Custom Icons:** Instead of Font Awesome for the finder section, create custom SVG icons that perfectly match the brand aesthetic.
7.  **Load Optimization:** Ensure images are optimized (correct format like WebP, appropriate size) for faster loading.

Above design provides a strong foundation that is visually appealing, unique compared to the sample, reflects the brand's mission, and incorporates elements designed to create a premium "Wow Effect." Remember to replace placeholder links (`#`) with actual page URLs as you build out the rest of the site.  
https://aistudio.google.com/app/prompts?state=%7B%22ids%22:%5B%2210PM7zv_w0EEcZ7USVqyiDHDaKKADlxcM%22%5D,%22action%22:%22open%22,%22userId%22:%22103961307342447084491%22,%22resourceKeys%22:%7B%7D%7D&usp=sharing
