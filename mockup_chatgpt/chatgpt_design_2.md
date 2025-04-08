Below is a carefully crafted **HTML + Tailwind CSS** example that emulates (and aims to surpass) the style of your attached image for both header and footer. It implements:

1. A **top header bar** announcing free shipping and a newsletter sign-up link.  
2. A **main header** row with your brand logo/name on the left, central nav links, and icons on the right (e.g., search, user, cart).  
3. A **footer** with a green-themed background, your brand mission, multiple link columns, a newsletter subscription, contact info, and payment method icons.  
4. A **“Follow Our Journey”** section (as a bridging element) just above the footer, inviting users to connect via Instagram.  

All colors, layout, and text can be adjusted to perfectly match your branding. The code below shows the essential structure and styling details.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="description" content="The Scent - Premium aromatherapy products for holistic well-being." />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>The Scent Aromatherapy</title>
  
  <!-- Tailwind CSS (CDN for demo) -->
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet" />

  <style>
    /* Adjust these color variables to match or surpass the attached design's palette */
    :root {
      --color-primary: #2F4D42; /* Main brand color */
      --color-secondary: #E88939; /* Accent highlight color */
      --color-dark-green: #2D5E4A; /* Footer background or highlight */
      --color-green-gradient-start: #224838;
      --color-green-gradient-end: #277053;
      --color-footer-text: #ECECEC;
    }
    body {
      font-family: 'Helvetica Neue', Arial, sans-serif;
    }

    /* Header styles */
    .header-topbar {
      background-color: var(--color-primary);
      color: #fff;
    }
    .header-main {
      box-shadow: 0 2px 4px rgba(0,0,0,0.08);
    }
    .header-nav a {
      transition: color 0.2s ease;
    }
    .header-nav a:hover {
      color: var(--color-secondary);
    }

    /* Footer styles */
    footer {
      background: linear-gradient(
        135deg, 
        var(--color-green-gradient-start) 0%, 
        var(--color-green-gradient-end) 100%
      );
      color: var(--color-footer-text);
    }
    footer a {
      color: var(--color-footer-text);
      transition: opacity 0.2s ease;
    }
    footer a:hover {
      opacity: 0.8;
    }
    /* Payment method icons can be sized consistently here */
    .payment-icon {
      width: 36px;
      height: auto;
    }
  </style>
</head>
<body class="text-gray-700">

<!-- HEADER -->
<!-- Top Bar -->
<div class="header-topbar w-full">
  <div class="max-w-7xl mx-auto flex items-center justify-between py-2 px-4 sm:px-6 lg:px-8 text-sm">
    <p>Free shipping on all orders over $50</p>
    <a href="#newsletter" class="underline hover:text-gray-100">Sign up for our newsletter & get 10% off</a>
  </div>
</div>

<!-- Main Header -->
<header class="header-main w-full bg-white">
  <div class="max-w-7xl mx-auto flex items-center justify-between py-4 px-4 sm:px-6 lg:px-8">
    <!-- Left: Logo or Brand Name -->
    <div class="text-xl md:text-2xl font-bold text-gray-800">
      The Scent Aromatherapy
    </div>

    <!-- Center: Main Navigation -->
    <nav class="header-nav hidden md:flex space-x-8 text-gray-600 text-sm font-medium">
      <a href="#home">Home</a>
      <a href="#shop">Shop</a>
      <a href="#scent-finder">Scent Finder</a>
      <a href="#our-story">Our Story</a>
      <a href="#contact">Contact</a>
    </nav>

    <!-- Right: Icons (Search, User, Cart) -->
    <div class="flex items-center space-x-4">
      <button aria-label="Search" class="text-gray-500 hover:text-gray-700">
        <!-- Use any icon library you prefer, e.g. Heroicons -->
        <svg class="w-5 h-5" fill="none" stroke="currentColor" stroke-width="2" 
             viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round">
          <circle cx="11" cy="11" r="8"></circle>
          <line x1="21" y1="21" x2="16.65" y2="16.65"></line>
        </svg>
      </button>
      <button aria-label="User Account" class="text-gray-500 hover:text-gray-700">
        <svg class="w-5 h-5" fill="none" stroke="currentColor" stroke-width="2" 
             viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round">
          <path d="M20 21v-2a4 4 0 00-3-3.87" />
          <path d="M4 21v-2a4 4 0 013-3.87" />
          <circle cx="12" cy="7" r="4" />
        </svg>
      </button>
      <button aria-label="View Cart" class="text-gray-500 hover:text-gray-700">
        <svg class="w-5 h-5" fill="none" stroke="currentColor" stroke-width="2" 
             viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round">
          <circle cx="9" cy="21" r="1"></circle>
          <circle cx="20" cy="21" r="1"></circle>
          <path d="M1 1h4l2.68 13.39a2 2 0 002 1.61h9.72a2 2 0 001.98-1.67L23 6H6" />
        </svg>
      </button>
    </div>
  </div>
</header>

<!-- OPTIONAL: Mobile Nav Toggle (hidden here, add if needed) -->

<!-- “FOLLOW OUR JOURNEY” SECTION -->
<section class="bg-white py-12">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
    <h2 class="text-2xl sm:text-3xl font-semibold text-gray-800 mb-2">Follow Our Journey</h2>
    <p class="text-gray-600 mb-6">
      Get inspired by our community and join the conversation. Follow us on Instagram 
      <span class="font-semibold text-gray-800">@TheScentAroma</span>
    </p>
    <div class="grid grid-cols-2 sm:grid-cols-4 md:grid-cols-6 gap-4">
      <!-- Example images pulled from your repository or placeholders -->
      <img src="https://raw.githubusercontent.com/nordeim/The-Scent/refs/heads/main/images/scent2.jpg" alt="Insta 1" class="w-full h-36 object-cover rounded" />
      <img src="https://raw.githubusercontent.com/nordeim/The-Scent/refs/heads/main/images/scent4.jpg" alt="Insta 2" class="w-full h-36 object-cover rounded" />
      <img src="https://raw.githubusercontent.com/nordeim/The-Scent/refs/heads/main/images/scent5.jpg" alt="Insta 3" class="w-full h-36 object-cover rounded" />
      <img src="https://raw.githubusercontent.com/nordeim/The-Scent/refs/heads/main/images/scent6.jpg" alt="Insta 4" class="w-full h-36 object-cover rounded" />
      <img src="https://raw.githubusercontent.com/nordeim/The-Scent/refs/heads/main/images/soap2.jpg" alt="Insta 5" class="w-full h-36 object-cover rounded hidden sm:block" />
      <img src="https://raw.githubusercontent.com/nordeim/The-Scent/refs/heads/main/images/soap6.jpg" alt="Insta 6" class="w-full h-36 object-cover rounded hidden sm:block" />
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer class="pt-16 pb-8">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 grid grid-cols-1 md:grid-cols-3 gap-8">
    <!-- 1. Brand & Description -->
    <div>
      <h3 class="text-lg font-bold mb-3">The Scent</h3>
      <p class="text-sm mb-4">
        We create premium aromatherapy products to enhance mental and 
        physical well-being through the power of scent.
      </p>
      <p class="text-xs mt-4">&copy; 2025 The Scent. All rights reserved.</p>
    </div>

    <!-- 2. Links -->
    <div class="flex justify-between md:block">
      <div class="mb-8">
        <h4 class="font-semibold mb-3">Shop</h4>
        <ul class="space-y-1 text-sm">
          <li><a href="#shop">Essential Oils</a></li>
          <li><a href="#shop">Natural Soaps</a></li>
          <li><a href="#shop">Gift Sets</a></li>
        </ul>
      </div>
      <div>
        <h4 class="font-semibold mb-3">Info</h4>
        <ul class="space-y-1 text-sm">
          <li><a href="#">FAQs</a></li>
          <li><a href="#">Shipping & Returns</a></li>
          <li><a href="#">Privacy Policy</a></li>
        </ul>
      </div>
    </div>

    <!-- 3. Contact & Newsletter -->
    <div>
      <h4 class="font-semibold mb-3">Contact Us</h4>
      <p class="text-sm">
        123 Aromatherapy Lane<br>
        Wellness City, WB 12345<br>
        +1 (123) 555-4567<br>
        hello@thescent.com
      </p>

      <!-- Newsletter subscription -->
      <div id="newsletter" class="mt-6">
        <h5 class="font-semibold mb-2">Subscribe to Newsletter</h5>
        <form class="flex space-x-2">
          <input 
            type="email" 
            placeholder="Enter your email" 
            class="flex-1 px-3 py-2 rounded focus:outline-none"
          >
          <button 
            type="submit" 
            class="bg-white text-green-700 font-medium px-5 py-2 rounded hover:bg-gray-100 transition"
          >
            Join
          </button>
        </form>
      </div>
    </div>
  </div>

  <!-- Payment Icons row -->
  <div class="mt-8 border-t border-green-200 pt-4">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex items-center justify-end space-x-4">
      <!-- Example payment icons (replace with your own) -->
      <img src="https://upload.wikimedia.org/wikipedia/commons/a/a4/Visa_2021.svg" alt="Visa" class="payment-icon" />
      <img src="https://upload.wikimedia.org/wikipedia/commons/5/5e/MasterCard_early_1990s_logo.png" alt="MasterCard" class="payment-icon" />
      <img src="https://upload.wikimedia.org/wikipedia/commons/0/04/PayPal_Logo.png" alt="PayPal" class="payment-icon h-4" />
    </div>
  </div>
</footer>

<!-- Optional Scripts -->
<script>
  // Toggle mobile nav, handle newsletter signups, etc., if needed
</script>

</body>
</html>
```

### Notable Highlights

1. **Multi-Level Header**  
   - **Top Bar:** Displays shipping and newsletter sign-up text.  
   - **Main Bar:** Showcases your brand name (or logo), central navigation menu, and icons on the right for search/user/cart.

2. **"Follow Our Journey" Section**  
   - Bold, centered heading and descriptive text.  
   - A grid of images to imitate an Instagram feed or your brand’s curated gallery.

3. **Footer with Green Gradient**  
   - Three-column layout reflecting your attached example: brand info, link sections, and contact details.  
   - A newsletter subscription form to capture user emails.  
   - Payment icons (Visa, MasterCard, PayPal, etc.) for professional e-commerce polish.

4. **Color & Visual Consistency**  
   - A cohesive, polished look that balances your brand’s green tones and accent colors.  
   - Typography and spacing reflect a modern, inviting atmosphere.

5. **Tailwind CSS Utility Classes**  
   - Allows rapid customization of spacing, layout, and color. Adapt color variables to perfectly match your brand or the reference design.

