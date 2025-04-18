\<think\>
Let me carefully analyze the existing HTML code and the company description to create an improved landing page for "The Scent" company.

First, I'll summarize what I understand about the business:
- Name: The Scent
- Focus: Aromatherapy products promoting mental & physical health
- Products: Essential oils and custom natural premium soaps
- Business model: Imports high-quality raw materials globally, creates unique formulations, exports finished products
- USP: Creative product formulations and deep knowledge of aromatherapy applications
- Positioning: Stress-reduction and wellness in an increasingly stressful world

The current website is using WordPress with the Avada theme and several plugins (LayerSlider, Contact Form 7, Projects by WooThemes, Revolution Slider). The code provided is partial, mostly containing the head section, but I can see from the meta description that the current landing page has basic sections about their products and company story.

For a "wow effect" landing page in the aromatherapy space, I'll focus on:
1. Creating a sensory experience through visuals (since websites can't transmit actual scents)
2. Using a soothing, organic design language with natural elements
3. Incorporating high-quality imagery of ingredients and products
4. Establishing an emotional connection immediately
5. Clearly communicating premium positioning and health benefits
6. Using subtle animations for visual interest
7. Ensuring mobile responsiveness

I'll design a completely new landing page with modern aesthetics while maintaining their brand focus on wellness and natural quality.
\<\/think\>

# Improved Landing Page for The Scent

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Scent | Premium Aromatherapy Solutions</title>
    <meta name="description" content="Discover The Scent's premium aromatherapy products crafted from the finest natural ingredients worldwide. Enhance your wellbeing through the power of scent.">
    
    <!-- Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;500;600;700&family=Montserrat:wght@300;400;500;600&display=swap" rel="stylesheet">
    
    <!-- Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --primary: #4A6F5D;
            --primary-light: #BDCFC6;
            --secondary: #E9D5C5;
            --accent: #C9A689;
            --dark: #2E3F38;
            --light: #F9F7F4;
            --white: #FFFFFF;
            --text: #333333;
            --transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        html {
            scroll-behavior: smooth;
        }
        
        body {
            font-family: 'Montserrat', sans-serif;
            line-height: 1.6;
            color: var(--text);
            background-color: var(--light);
            overflow-x: hidden;
        }
        
        h1, h2, h3, h4 {
            font-family: 'Cormorant Garamond', serif;
            font-weight: 600;
            line-height: 1.3;
            color: var(--dark);
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .btn {
            display: inline-block;
            padding: 14px 32px;
            border-radius: 50px;
            font-weight: 500;
            transition: var(--transition);
            cursor: pointer;
            position: relative;
            overflow: hidden;
            font-size: 15px;
            letter-spacing: 1px;
            text-transform: uppercase;
            text-decoration: none;
        }
        
        .btn-primary {
            background-color: var(--primary);
            color: var(--white);
            box-shadow: 0 6px 20px rgba(74, 111, 93, 0.25);
        }
        
        .btn-primary:hover {
            background-color: var(--dark);
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(46, 63, 56, 0.3);
        }
        
        .btn-outline {
            background-color: transparent;
            color: var(--primary);
            border: 2px solid var(--primary);
        }
        
        .btn-outline:hover {
            background-color: var(--primary);
            color: var(--white);
            transform: translateY(-3px);
        }
        
        /* Header */
        header {
            position: fixed;
            width: 100%;
            z-index: 1000;
            padding: 20px 0;
            transition: var(--transition);
        }
        
        header.scrolled {
            background-color: var(--white);
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.08);
            padding: 15px 0;
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo-text {
            font-family: 'Cormorant Garamond', serif;
            font-size: 28px;
            font-weight: 700;
            color: var(--dark);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
            gap: 40px;
        }
        
        .nav-links a {
            font-weight: 500;
            font-size: 14px;
            letter-spacing: 1px;
            text-transform: uppercase;
            color: var(--dark);
            text-decoration: none;
            position: relative;
        }
        
        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -4px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--primary);
            transition: var(--transition);
        }
        
        .nav-links a:hover::after {
            width: 100%;
        }
        
        .nav-cta {
            margin-left: 20px;
        }
        
        .mobile-toggle {
            display: none;
            cursor: pointer;
            z-index: 1001;
        }
        
        .mobile-toggle span {
            display: block;
            width: 25px;
            height: 2px;
            margin: 5px 0;
            background-color: var(--dark);
            transition: var(--transition);
        }
        
        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            background-color: var(--light);
            position: relative;
            overflow: hidden;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 50%;
            height: 100%;
            background-color: var(--primary-light);
            opacity: 0.2;
            clip-path: polygon(20% 0%, 100% 0%, 100% 100%, 0% 100%);
        }
        
        .hero-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            align-items: center;
            gap: 60px;
            position: relative;
        }
        
        .hero-text h1 {
            font-size: 72px;
            margin-bottom: 24px;
            line-height: 1.1;
            color: var(--dark);
        }
        
        .hero-text h1 span {
            color: var(--primary);
        }
        
        .hero-text p {
            font-size: 18px;
            margin-bottom: 35px;
            color: #555;
            max-width: 500px;
        }
        
        .hero-buttons {
            display: flex;
            gap: 15px;
        }
        
        .hero-image-container {
            position: relative;
        }
        
        .hero-image {
            width: 100%;
            border-radius: 30px;
            box-shadow: 30px 30px 80px rgba(0, 0, 0, 0.1);
            position: relative;
            z-index: 2;
        }
        
        .floating-element {
            position: absolute;
            z-index: 1;
            animation: float 6s ease-in-out infinite;
        }
        
        .leaf-1 {
            top: -20px;
            left: -10%;
            width: 120px;
            animation-delay: 0s;
        }
        
        .leaf-2 {
            bottom: 10%;
            right: -5%;
            width: 100px;
            animation-delay: 1s;
        }
        
        .drop-1 {
            top: 20%;
            left: -8%;
            width: 35px;
            animation-delay: 2s;
        }
        
        .drop-2 {
            bottom: 15%;
            left: 10%;
            width: 25px;
            animation-delay: 1.5s;
        }
        
        @keyframes float {
            0% { transform: translateY(0) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(5deg); }
            100% { transform: translateY(0) rotate(0deg); }
        }
        
        .scroll-indicator {
            position: absolute;
            bottom: 40px;
            left: 50%;
            transform: translateX(-50%);
            display: flex;
            flex-direction: column;
            align-items: center;
            cursor: pointer;
            z-index: 2;
        }
        
        .scroll-indicator span {
            font-size: 12px;
            letter-spacing: 2px;
            text-transform: uppercase;
            margin-bottom: 8px;
        }
        
        .scroll-indicator i {
            animation: bounce 2s infinite;
        }
        
        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
            40% { transform: translateY(-10px); }
            60% { transform: translateY(-5px); }
        }
        
        /* About Section */
        .about {
            padding: 120px 0;
            background-color: var(--white);
            position: relative;
        }
        
        .section-title-container {
            text-align: center;
            margin-bottom: 60px;
        }
        
        .section-subtitle {
            display: inline-block;
            font-size: 14px;
            font-weight: 500;
            letter-spacing: 2px;
            text-transform: uppercase;
            color: var(--primary);
            margin-bottom: 15px;
            position: relative;
        }
        
        .section-subtitle::before,
        .section-subtitle::after {
            content: '';
            position: absolute;
            top: 50%;
            width: 30px;
            height: 1px;
            background-color: var(--primary);
        }
        
        .section-subtitle::before {
            left: -40px;
        }
        
        .section-subtitle::after {
            right: -40px;
        }
        
        .section-title {
            font-size: 48px;
            color: var(--dark);
            margin-bottom: 20px;
        }
        
        .section-description {
            max-width: 700px;
            margin: 0 auto;
            color: #555;
        }
        
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
            margin-top: 60px;
        }
        
        .about-image-container {
            position: relative;
        }
        
        .about-image {
            width: 100%;
            border-radius: 20px;
            box-shadow: 20px 20px 60px rgba(0, 0, 0, 0.1);
        }
        
        .experience-badge {
            position: absolute;
            right: -30px;
            bottom: -30px;
            width: 160px;
            height: 160px;
            background-color: var(--primary);
            color: var(--white);
            border-radius: 50%;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            box-shadow: 10px 10px 30px rgba(74, 111, 93, 0.3);
        }
        
        .experience-badge .number {
            font-family: 'Cormorant Garamond', serif;
            font-size: 60px;
            line-height: 1;
            font-weight: 600;
        }
        
        .experience-badge .text {
            font-size: 14px;
            letter-spacing: 1px;
            text-transform: uppercase;
        }
        
        .about-text h3 {
            font-size: 36px;
            margin-bottom: 25px;
        }
        
        .about-text p {
            margin-bottom: 20px;
            color: #555;
        }
        
        .about-features {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
            margin-top: 30px;
        }
        
        .about-feature {
            display: flex;
            align-items: flex-start;
            gap: 15px;
        }
        
        .about-feature i {
            color: var(--primary);
            font-size: 24px;
        }
        
        .about-feature h4 {
            font-size: 18px;
            margin-bottom: 5px;
        }
        
        .about-feature p {
            font-size: 14px;
            margin-bottom: 0;
        }
        
        /* Products Section */
        .products {
            padding: 120px 0;
            background-color: var(--light);
            position: relative;
            overflow: hidden;
        }
        
        .products-background {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: url('data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxMDAlIiBoZWlnaHQ9IjEwMCUiPjxkZWZzPjxwYXR0ZXJuIGlkPSJwYXR0ZXJuIiB3aWR0aD0iNDAiIGhlaWdodD0iNDAiIHZpZXdCb3g9IjAgMCA0MCA0MCIgcGF0dGVyblVuaXRzPSJ1c2VyU3BhY2VPblVzZSIgcGF0dGVyblRyYW5zZm9ybT0icm90YXRlKDQ1KSI+PHJlY3QgaWQ9InBhdHRlcm4tYmFja2dyb3VuZCIgd2lkdGg9IjQwMCUiIGhlaWdodD0iNDAwJSIgZmlsbD0idHJhbnNwYXJlbnQiPjwvcmVjdD48Y2lyY2xlIGN4PSIyMCIgY3k9IjIwIiByPSIxIiBmaWxsPSIjNEE2RjVEIiBmaWxsLW9wYWNpdHk9IjAuMDUiPjwvY2lyY2xlPjwvcGF0dGVybj48L2RlZnM+PHJlY3QgZmlsbD0idXJsKCNwYXR0ZXJuKSIgaGVpZ2h0PSIxMDAlIiB3aWR0aD0iMTAwJSI+PC9yZWN0Pjwvc3ZnPg==');
            opacity: 0.6;
        }
        
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            margin-top: 60px;
        }
        
        .product-card {
            background-color: var(--white);
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.05);
            transition: var(--transition);
            position: relative;
        }
        
        .product-card:hover {
            transform: translateY(-15px);
            box-shadow: 0 30px 60px rgba(0, 0, 0, 0.1);
        }
        
        .product-image {
            height: 280px;
            overflow: hidden;
            position: relative;
        }
        
        .product-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
        }
        
        .product-card:hover .product-image img {
            transform: scale(1.1);
        }
        
        .product-badge {
            position: absolute;
            top: 20px;
            right: 20px;
            background-color: var(--accent);
            color: var(--white);
            padding: 5px 15px;
            border-radius: 50px;
            font-size: 12px;
            text-transform: uppercase;
            letter-spacing: 1px;
            font-weight: 500;
        }
        
        .product-info {
            padding: 30px;
        }
        
        .product-title {
            font-size: 24px;
            margin-bottom: 10px;
        }
        
        .product-description {
            color: #666;
            font-size: 15px;
            margin-bottom: 15px;
        }
        
        .product-meta {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: 20px;
        }
        
        .product-price {
            font-family: 'Cormorant Garamond', serif;
            font-size: 24px;
            font-weight: 600;
            color: var(--primary);
        }
        
        .product-action {
            width: 45px;
            height: 45px;
            background-color: var(--primary-light);
            color: var(--dark);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: var(--transition);
        }
        
        .product-action:hover {
            background-color: var(--primary);
            color: var(--white);
        }
        
        /* Benefits Section */
        .benefits {
            padding: 120px 0;
            background-color: var(--dark);
            position: relative;
            color: var(--white);
            overflow: hidden;
        }
        
        .benefits::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, rgba(74, 111, 93, 0.3) 0%, transparent 50%);
        }
        
        .benefits .section-title {
            color: var(--white);
        }
        
        .benefits-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 60px;
            position: relative;
            z-index: 2;
        }
        
        .benefit-card {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px 30px;
            transition: var(--transition);
            border: 1px solid rgba(255, 255, 255, 0.1);
            height: 100%;
        }
        
        .benefit-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
            background: rgba(255, 255, 255, 0.08);
        }
        
        .benefit-icon {
            margin-bottom: 25px;
            color: var(--accent);
            font-size: 40px;
        }
        
        .benefit-title {
            font-size: 24px;
            margin-bottom: 15px;
            color: var(--white);
        }
        
        .benefit-description {
            color: rgba(255, 255, 255, 0.8);
            font-size: 15px;
        }
        
        /* Testimonials */
        .testimonials {
            padding: 120px 0;
            background-color: var(--white);
            position: relative;
        }
        
        .testimonial-card {
            background-color: var(--light);
            border-radius: 20px;
            padding: 40px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.05);
            text-align: center;
            position: relative;
            max-width: 800px;
            margin: 60px auto 0;
        }
        
        .testimonial-card::before {
            content: '"';
            position: absolute;
            top: 20px;
            left: 30px;
            font-family: 'Cormorant Garamond', serif;
            font-size: 120px;
            line-height: 1;
            color: var(--primary-light);
            opacity: 0.5;
        }
        
        .testimonial-text {
            font-size: 20px;
            line-height: 1.7;
            color: var(--dark);
            margin-bottom: 30px;
            position: relative;
            z-index: 1;
        }
        
        .testimonial-author {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .author-image {
            width: 70px;
            height: 70px;
            border-radius: 50%;
            overflow: hidden;
            margin-bottom: 15px;
            border: 3px solid var(--white);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .author-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .author-name {
            font-size: 18px;
            font-weight: 600;
            margin-bottom: 5px;
        }
        
        .author-title {
            font-size: 14px;
            color: #666;
        }
        
        /* CTA Section */
        .cta {
            padding: 120px 0;
            background-color: var(--primary);
            color: var(--white);
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .cta::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSI1MCIgaGVpZ2h0PSI1MCI+PGNpcmNsZSBjeD0iMjUiIGN5PSIyNSIgcj0iMSIgZmlsbD0iI2ZmZiIgZmlsbC1vcGFjaXR5PSIwLjEiLz48L3N2Zz4=');
            opacity: 0.4;
        }
        
        .cta-content {
            position: relative;
            z-index: 1;
            max-width: 700px;
            margin: 0 auto;
        }
        
        .cta-title {
            font-size: 48px;
            margin-bottom: 20px;
            color: var(--white);
        }
        
        .cta-text {
            font-size: 18px;
            margin-bottom: 40px;
            color: rgba(255, 255, 255, 0.9);
        }
        
        .btn-light {
            background-color: var(--white);
            color: var(--primary);
        }
        
        .btn-light:hover {
            background-color: var(--secondary);
            color: var(--dark);
            transform: translateY(-3px);
            box-shadow: 0 10px 30px rgba(255, 255, 255, 0.2);
        }
        
        /* Footer */
        .footer {
            background-color: var(--dark);
            color: var(--white);
            padding: 80px 0 30px;
            position: relative;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1fr;
            gap: 40px;
            margin-bottom: 60px;
        }
        
        .footer-logo {
            font-family: 'Cormorant Garamond', serif;
            font-size: 28px;
            font-weight: 700;
            margin-bottom: 20px;
            color: var(--white);
        }
        
        .footer-about {
            color: rgba(255, 255, 255, 0.7);
            margin-bottom: 25px;
            font-size: 15px;
            max-width: 300px;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
        }
        
        .social-link {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            background-color: rgba(255, 255, 255, 0.1);
            color: var(--white);
            transition: var(--transition);
        }
        
        .social-link:hover {
            background-color: var(--primary);
            transform: translateY(-3px);
        }
        
        .footer-heading {
            font-size: 18px;
            margin-bottom: 25px;
            color: var(--white);
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 10px;
        }
        
        .footer-links a {
            color: rgba(255, 255, 255, 0.7);
            text-decoration: none;
            transition: var(--transition);
            font-size: 15px;
        }
        
        .footer-links a:hover {
            color: var(--white);
            padding-left: 5px;
        }
        
        .footer-contact-item {
            display: flex;
            align-items: flex-start;
            gap: 15px;
            margin-bottom: 15px;
            color: rgba(255, 255, 255, 0.7);
        }
        
        .footer-contact-item i {
            color: var(--primary-light);
        }
        
        .footer-bottom {
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            padding-top: 30px;
            text-align: center;
            color: rgba(255, 255, 255, 0.5);
            font-size: 14px;
        }
        
        /* Responsive Styles */
        @media screen and (max-width: 992px) {
            .hero-text h1 {
                font-size: 56px;
            }
            
            .footer-content {
                grid-template-columns: 1fr 1fr;
            }
        }
        
        @media screen and (max-width: 768px) {
            .mobile-toggle {
                display: block;
            }
            
            .nav-links {
                position: fixed;
                top: 0;
                right: -100%;
                width: 70%;
                height: 100vh;
                background-color: var(--white);
                flex-direction: column;
                justify-content: center;
                align-items: center;
                transition: var(--transition);
                box-shadow: -10px 0 30px rgba(0, 0, 0, 0.1);
            }
            
            .nav-links.active {
                right: 0;
            }
            
            .hero-content,
            .about-content {
                grid-template-columns: 1fr;
                text-align: center;
            }
            
            .hero-text h1 {
                font-size: 48px;
            }
            
            .hero-text p {
                margin: 0 auto 35px;
            }
            
            .hero-buttons {
                justify-content: center;
            }
            
            .section-title {
                font-size: 40px;
            }
            
            .about-image-container {
                order: -1;
                margin-bottom: 30px;
            }
            
            .about-features {
                grid-template-columns: 1fr;
            }
            
            .experience-badge {
                right: 50%;
                transform: translateX(50%);
            }
        }
        
        @media screen and (max-width: 576px) {
            .hero-text h1 {
                font-size: 36px;
            }
            
            .section-title {
                font-size: 32px;
            }
            
            .cta-title {
                font-size: 36px;
            }
            
            .testimonial-card {
                padding: 30px 20px;
            }
            
            .footer-content {
                grid-template-columns: 1fr;
                gap: 30px;
            }
            
            .footer-about {
                max-width: 100%;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header id="header">
        <div class="container">
            <nav>
                <div class="logo">
                    <div class="logo-text">The Scent</div>
                </div>
                
                <ul class="nav-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#products">Products</a></li>
                    <li><a href="#benefits">Benefits</a></li>
                    <li><a href="#testimonials">Testimonials</a></li>
                    <li><a href="#contact" class="nav-cta btn btn-primary">Contact</a></li>
                </ul>
                
                <div class="mobile-toggle">
                    <span></span>
                    <span></span>
                    <span></span>
                </div>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container hero-content">
            <div class="hero-text">
                <h1>Discover the <span>Essence</span> of Wellbeing</h1>
                <p>Premium aromatherapy products crafted with the finest natural ingredients from around the world to enhance your mental & physical health.</p>
                <div class="hero-buttons">
                    <a href="#products" class="btn btn-primary">Explore Collection</a>
                    <a href="#about" class="btn btn-outline">Our Story</a>
                </div>
            </div>
            
            <div class="hero-image-container">
                <img src="https://images.unsplash.com/photo-1594631864763-7b71839529a1?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Premium Essential Oils Collection" class="hero-image">
                
                <img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTUwIiBoZWlnaHQ9IjE1MCIgdmlld0JveD0iMCAwIDI0IDI0IiBmaWxsPSJub25lIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxwYXRoIGQ9Ik0xMiA0QzEyIDQgNyAxMCA0IDE1QzEgMjAgNyAyMiAxMiAyMkMxNyAyMiAyMyAyMCAyMCAxNUMxNyAxMCAxMiA0IDEyIDRaIiBmaWxsPSIjQkRDRkM2IiBzdHJva2U9IiM0QTZGNUQiIHN0cm9rZS13aWR0aD0iMC41Ii8+PC9zdmc+" alt="" class="floating-element leaf-1">
                
                <img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTUwIiBoZWlnaHQ9IjE1MCIgdmlld0JveD0iMCAwIDI0IDI0IiBmaWxsPSJub25lIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxwYXRoIGQ9Ik04IDRDOCA0IDMgOSA0IDE1QzUgMjEgMTIgMjIgMTYgMThDMjAgMTQgMTMgNCA4IDRaIiBmaWxsPSIjQkRDRkM2IiBzdHJva2U9IiM0QTZGNUQiIHN0cm9rZS13aWR0aD0iMC41Ii8+PC9zdmc+" alt="" class="floating-element leaf-2">
                
                <img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNDAiIGhlaWdodD0iNDAiIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48cGF0aCBkPSJNMTIgNUMxMiA1IDkgNyA5IDEyQzkgMTcgMTIgMTkgMTIgMTlDMTIgMTkgMTUgMTcgMTUgMTJDMTUgNyAxMiA1IDEyIDVaIiBmaWxsPSIjRTlENUM1IiBzdHJva2U9IiNDOUE2ODkiIHN0cm9rZS13aWR0aD0iMC41Ii8+PC9zdmc+" alt="" class="floating-element drop-1">
                
                <img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMzAiIGhlaWdodD0iMzAiIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48cGF0aCBkPSJNMTIgNUMxMiA1IDkgNyA5IDEyQzkgMTcgMTIgMTkgMTIgMTlDMTIgMTkgMTUgMTcgMTUgMTJDMTUgNyAxMiA1IDEyIDVaIiBmaWxsPSIjRTlENUM1IiBzdHJva2U9IiNDOUE2ODkiIHN0cm9rZS13aWR0aD0iMC41Ii8+PC9zdmc+" alt="" class="floating-element drop-2">
            </div>
        </div>
        
        <div class="scroll-indicator">
            <span>Scroll Down</span>
            <i class="fas fa-chevron-down"></i>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <div class="section-title-container">
                <span class="section-subtitle">Our Story</span>
                <h2 class="section-title">The Journey of Scent</h2>
                <p class="section-description">Discover the passion and expertise behind our premium aromatherapy products.</p>
            </div>
            
            <div class="about-content">
                <div class="about-image-container">
                    <img src="https://images.unsplash.com/photo-1543362906-acfc16c67564?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="The Scent Workspace" class="about-image">
                    <div class="experience-badge">
                        <span class="number">15</span>
                        <span class="text">Years of Excellence</span>
                    </div>
                </div>
                
                <div class="about-text">
                    <h3>Enhancing Lives Through Aromatherapy</h3>
                    <p>Our company produces a whole range of aroma therapeutic products where high-quality raw materials from all over the world are imported and our finished products are exported back to these countries.</p>
                    <p>This is possible due to our unique and creative product formulations and our knowledge for the various applications, to create harmonious, balanced and well-rounded aromatherapy products.</p>
                    <p>Stress is an ever-increasing part of our lives, and this can only mean that aromatherapy is more relevant today than ever before.</p>
                    
                    <div class="about-features">
                        <div class="about-feature">
                            <i class="fas fa-leaf"></i>
                            <div>
                                <h4>Natural Ingredients</h4>
                                <p>Sourced from the finest global suppliers</p>
                            </div>
                        </div>
                        
                        <div class="about-feature">
                            <i class="fas fa-flask"></i>
                            <div>
                                <h4>Expert Formulations</h4>
                                <p>Uniquely crafted by our aromatherapy specialists</p>
                            </div>
                        </div>
                        
                        <div class="about-feature">
                            <i class="fas fa-heart"></i>
                            <div>
                                <h4>Wellness Focused</h4>
                                <p>Promoting both mental and physical health</p>
                            </div>
                        </div>
                        
                        <div class="about-feature">
                            <i class="fas fa-globe-asia"></i>
                            <div>
                                <h4>Global Reach</h4>
                                <p>Serving customers across the world</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Products Section -->
    <section id="products" class="products">
        <div class="products-background"></div>
        <div class="container">
            <div class="section-title-container">
                <span class="section-subtitle">Our Collection</span>
                <h2 class="section-title">Premium Aromatherapy Products</h2>
                <p class="section-description">Explore our curated selection of essential oils and natural soaps, designed to enhance your wellbeing.</p>
            </div>
            
            <div class="products-grid">
                <div class="product-card">
                    <div class="product-image">
                        <img src="https://images.unsplash.com/photo-1608571423902-eed4a5ad8108?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Lavender Essential Oil">
                        <div class="product-badge">Bestseller</div>
                    </div>
                    <div class="product-info">
                        <h3 class="product-title">Lavender Essential Oil</h3>
                        <p class="product-description">Pure lavender oil to promote relaxation and better sleep quality. Sourced from organic farms.</p>
                        <div class="product-meta">
                            <div class="product-price">$29.95</div>
                            <div class="product-action">
                                <i class="fas fa-shopping-bag"></i>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="product-card">
                    <div class="product-image">
                        <img src="https://images.unsplash.com/photo-1505740420928-5e560c06d30e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Citrus Blend">
                        <div class="product-badge">New</div>
                    </div>
                    <div class="product-info">
                        <h3 class="product-title">Citrus Awakening Blend</h3>
                        <p class="product-description">Energizing blend of orange, lemon, and grapefruit to invigorate your senses and boost your mood.</p>
                        <div class="product-meta">
                            <div class="product-price">$34.95</div>
                            <div class="product-action">
                                <i class="fas fa-shopping-bag"></i>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="product-card">
                    <div class="product-image">
                        <img src="https://images.unsplash.com/photo-1541256942802-2b8b24403016?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Handcrafted Soap Collection">
                    </div>
                    <div class="product-info">
                        <h3 class="product-title">Natural Artisan Soap</h3>
                        <p class="product-description">Handcrafted soaps made with essential oils and botanical ingredients for a luxurious cleansing experience.</p>
                        <div class="product-meta">
                            <div class="product-price">$12.95</div>
                            <div class="product-action">
                                <i class="fas fa-shopping-bag"></i>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="product-card">
                    <div class="product-image">
                        <img src="https://images.unsplash.com/photo-1547887538-e3a2f32cb1cc?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Wellness Gift Set">
                        <div class="product-badge">Popular</div>
                    </div>
                    <div class="product-info">
                        <h3 class="product-title">Complete Wellness Set</h3>
                        <p class="product-description">A curated collection of our most popular essential oils and soaps, perfect as a gift or for self-care.</p>
                        <div class="product-meta">
                            <div class="product-price">$89.95</div>
                            <div class="product-action">
                                <i class="fas fa-shopping-bag"></i>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Benefits Section -->
    <section id="benefits" class="benefits">
        <div class="container">
            <div class="section-title-container">
                <span class="section-subtitle">Why Choose Us</span>
                <h2 class="section-title">The Power of Aromatherapy</h2>
                <p class="section-description">Experience how our products can transform your wellbeing through the science of scent.</p>
            </div>
            
            <div class="benefits-grid">
                <div class="benefit-card">
                    <div class="benefit-icon">
                        <i class="fas fa-brain"></i>
                    </div>
                    <h3 class="benefit-title">Stress Relief</h3>
                    <p class="benefit-description">Our carefully formulated aromatherapy products help reduce stress and anxiety, promoting a sense of calm and relaxation in your daily life.</p>
                </div>
                
                <div class="benefit-card">
                    <div class="benefit-icon">
                        <i class="fas fa-moon"></i>
                    </div>
                    <h3 class="benefit-title">Improved Sleep</h3>
                    <p class="benefit-description">Experience deeper, more restful sleep with our sleep-enhancing scents that help quiet the mind and prepare the body for restorative rest.</p>
                </div>
                
                <div class="benefit-card">
                    <div class="benefit-icon">
                        <i class="fas fa-smile"></i>
                    </div>
                    <h3 class="benefit-title">Mood Enhancement</h3>
                    <p class="benefit-description">Elevate your mood and mental wellbeing with uplifting scents that can help combat feelings of sadness and promote positive emotions.</p>
                </div>
                
                <div class="benefit-card">
                    <div class="benefit-icon">
                        <i class="fas fa-heartbeat"></i>
                    </div>
                    <h3 class="benefit-title">Physical Wellness</h3>
                    <p class="benefit-description">Many of our essential oils offer benefits for physical wellness, from easing muscle tension to supporting respiratory health.</p>
                </div>
                
                <div class="benefit-card">
                    <div class="benefit-icon">
                        <i class="fas fa-leaf"></i>
                    </div>
                    <h3 class="benefit-title">100% Natural</h3>
                    <p class="benefit-description">We use only the purest natural ingredients, free from synthetic chemicals, ensuring that our products are gentle on your body and the environment.</p>
                </div>
                
                <div class="benefit-card">
                    <div class="benefit-icon">
                        <i class="fas fa-lightbulb"></i>
                    </div>
                    <h3 class="benefit-title">Focus & Clarity</h3>
                    <p class="benefit-description">Certain aromas can help improve mental clarity, focus, and cognitive performance, making them perfect for work or study environments.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section id="testimonials" class="testimonials">
        <div class="container">
            <div class="section-title-container">
                <span class="section-subtitle">Customer Stories</span>
                <h2 class="section-title">What People Say</h2>
                <p class="section-description">Hear from those who have experienced the transformative power of our aromatherapy products.</p>
            </div>
            
            <div class="testimonial-card">
                <p class="testimonial-text">"I've been using The Scent's essential oils for over a year now, and the difference they've made in my life is remarkable. Their lavender oil has transformed my sleep quality, and their citrus blend gets me through my workday with renewed energy. The natural, pure quality of these products is unmatched."</p>
                
                <div class="testimonial-author">
                    <div class="author-image">
                        <img src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=256&q=80" alt="Sarah Johnson">
                    </div>
                    <h4 class="author-name">Sarah Johnson</h4>
                    <p class="author-title">Wellness Coach, Singapore</p>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="cta">
        <div class="container">
            <div class="cta-content">
                <h2 class="cta-title">Transform Your Wellbeing</h2>
                <p class="cta-text">Join thousands of satisfied customers who have discovered the power of aromatherapy with our premium products.</p>
                <a href="#products" class="btn btn-light">Shop Now</a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contact" class="footer">
        <div class="container">
            <div class="footer-content">
                <div>
                    <div class="footer-logo">The Scent</div>
                    <p class="footer-about">Our mission is to promote mental and physical health through the power of aromatherapy, using only the finest natural ingredients from around the world.</p>
                    <div class="social-links">
                        <a href="#" class="social-link"><i class="fab fa-facebook-f"></i></a>
                        <a href="#" class="social-link"><i class="fab fa-instagram"></i></a>
                        <a href="#" class="social-link"><i class="fab fa-pinterest-p"></i></a>
                        <a href="#" class="social-link"><i class="fab fa-twitter"></i></a>
                    </div>
                </div>
                
                <div>
                    <h3 class="footer-heading">Quick Links</h3>
                    <ul class="footer-links">
                        <li><a href="#home">Home</a></li>
                        <li><a href="#about">About Us</a></li>
                        <li><a href="#products">Shop</a></li>
                        <li><a href="#benefits">Benefits</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>
                
                <div>
                    <h3 class="footer-heading">Our Products</h3>
                    <ul class="footer-links">
                        <li><a href="#">Essential Oils</a></li>
                        <li><a href="#">Natural Soaps</a></li>
                        <li><a href="#">Gift Sets</a></li>
                        <li><a href="#">Oil Diffusers</a></li>
                        <li><a href="#">Aromatherapy Guides</a></li>
                    </ul>
                </div>
                
                <div>
                    <h3 class="footer-heading">Contact Us</h3>
                    <div class="footer-contact-item">
                        <i class="fas fa-map-marker-alt"></i>
                        <span>123 Aromatherapy Street, Singapore 123456</span>
                    </div>
                    <div class="footer-contact-item">
                        <i class="fas fa-phone"></i>
                        <span>+65 9876 5432</span>
                    </div>
                    <div class="footer-contact-item">
                        <i class="fas fa-envelope"></i>
                        <span>hello@thescent.com.sg</span>
                    </div>
                </div>
            </div>
            
            <div class="footer-bottom">
                <p>&copy; 2025 The Scent. All Rights Reserved.</p>
            </div>
        </div>
    </footer>

    <!-- JavaScript -->
    <script>
        // Mobile Navigation Toggle
        const mobileToggle = document.querySelector('.mobile-toggle');
        const navLinks = document.querySelector('.nav-links');
        
        mobileToggle.addEventListener('click', () => {
            navLinks.classList.toggle('active');
            mobileToggle.classList.toggle('active');
        });
        
        // Header Scroll Effect
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        });
        
        // Smooth Scrolling for Anchor Links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                if (navLinks.classList.contains('active')) {
                    navLinks.classList.remove('active');
                    mobileToggle.classList.remove('active');
                }
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
```

Would you like me to explain or break down the code?
