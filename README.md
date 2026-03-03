<html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Velvet & Silk | Premium Saree Store</title>
    <!-- Google Fonts for Elegance -->
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=Lato:wght@300;400;700&display=swap" rel="stylesheet">
    <!-- Font Awesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    
    <style>
        /* --- CSS Variables & Reset --- */
        :root {
            --primary-maroon: #800000;
            --dark-maroon: #5a0000;
            --bg-white: #FFFFFF;
            --text-dark: #333333;
            --text-light: #666666;
            --light-grey: #f9f9f9;
            --border-color: #e0e0e0;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Lato', sans-serif;
            background-color: var(--bg-white);
            color: var(--text-dark);
            line-height: 1.6;
            /* Subtle traditional pattern overlay */
            background-image: radial-gradient(#e0e0e0 1px, transparent 1px);
            background-size: 20px 20px;
        }

        h1, h2, h3, h4 {
            font-family: 'Playfair Display', serif;
            color: var(--primary-maroon);
        }

        a {
            text-decoration: none;
            color: inherit;
            transition: 0.3s;
        }

        ul {
            list-style: none;
        }

        /* --- Header Section --- */
        header {
            background-color: var(--bg-white);
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            position: sticky;
            top: 0;
            z-index: 1000;
            border-bottom: 3px solid var(--primary-maroon);
        }

        .navbar {
            max-width: 1200px;
            margin: 0 auto;
            padding: 1rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            font-family: 'Playfair Display', serif;
            color: var(--primary-maroon);
            letter-spacing: 1px;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
        }

        .nav-links a {
            font-weight: 600;
            font-size: 0.95rem;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            color: var(--text-dark);
        }

        .nav-links a:hover {
            color: var(--primary-maroon);
        }

        .search-bar {
            position: relative;
        }

        .search-bar input {
            padding: 8px 15px;
            border: 1px solid var(--primary-maroon);
            border-radius: 20px;
            outline: none;
            font-family: 'Lato', sans-serif;
        }

        .search-bar button {
            position: absolute;
            right: 5px;
            top: 50%;
            transform: translateY(-50%);
            background: none;
            border: none;
            color: var(--primary-maroon);
            cursor: pointer;
        }

        /* --- Hero Section --- */
        .hero {
            height: 80vh;
            background: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.3)), url('https://images.unsplash.com/photo-1610189012906-4783382c508d?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
        }

        .hero-content h1 {
            font-size: 4rem;
            color: white;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }

        .hero-content p {
            font-size: 1.5rem;
            font-style: italic;
            margin-bottom: 2rem;
            font-family: 'Playfair Display', serif;
        }

        .btn {
            padding: 12px 30px;
            background-color: var(--primary-maroon);
            color: white;
            border: none;
            font-size: 1rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            cursor: pointer;
            transition: background 0.3s ease;
            display: inline-block;
        }

        .btn:hover {
            background-color: var(--dark-maroon);
        }

        /* --- Categories Dropdown --- */
        .category-section {
            background-color: var(--light-grey);
            padding: 2rem 0;
            text-align: center;
            border-bottom: 1px solid var(--border-color);
        }

        .category-container {
            max-width: 1200px;
            margin: 0 auto;
            position: relative;
            display: inline-block;
        }

        .category-btn {
            background: none;
            border: 1px solid var(--primary-maroon);
            color: var(--primary-maroon);
            padding: 10px 20px;
            cursor: pointer;
            font-family: 'Playfair Display', serif;
            font-size: 1.1rem;
        }

        .dropdown-content {
            display: none;
            position: absolute;
            background-color: var(--bg-white);
            min-width: 200px;
            box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.1);
            z-index: 1;
            top: 100%;
            left: 0;
            border-top: 3px solid var(--primary-maroon);
        }

        .dropdown-content a {
            color: var(--text-dark);
            padding: 12px 16px;
            text-decoration: none;
            display: block;
            text-align: left;
            border-bottom: 1px solid #eee;
        }

        .dropdown-content a:hover {
            background-color: var(--light-grey);
            color: var(--primary-maroon);
        }

        .category-container:hover .dropdown-content {
            display: block;
        }

        /* --- Product Section --- */
        .products-section {
            max-width: 1200px;
            margin: 4rem auto;
            padding: 0 2rem;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 60px;
            height: 3px;
            background-color: var(--primary-maroon);
            margin: 10px auto 0;
        }

        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .product-card {
            background: white;
            border: 1px solid var(--border-color);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            overflow: hidden;
        }

        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }

        .product-image {
            width: 100%;
            height: 350px;
            object-fit: cover;
            background-color: #f0f0f0;
        }

        .product-info {
            padding: 1.5rem;
            text-align: center;
        }

        .product-name {
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
            color: var(--text-dark);
        }

        .product-price {
            font-size: 1.1rem;
            color: var(--primary-maroon);
            font-weight: 700;
            margin-bottom: 1rem;
        }

        .card-buttons {
            display: flex;
            gap: 10px;
            justify-content: center;
        }

        .btn-outline {
            background: transparent;
            border: 1px solid var(--primary-maroon);
            color: var(--primary-maroon);
            padding: 8px 15px;
            cursor: pointer;
            transition: 0.3s;
        }

        .btn-outline:hover {
            background: var(--primary-maroon);
            color: white;
        }

        /* --- Entry Form Section --- */
        .admin-section {
            background-color: var(--light-grey);
            padding: 4rem 2rem;
            margin-top: 4rem;
        }

        .form-container {
            max-width: 600px;
            margin: 0 auto;
            background: white;
            padding: 2rem;
            border-radius: 5px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            border-top: 4px solid var(--primary-maroon);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            color: var(--text-dark);
        }

        .form-group input, 
        .form-group select, 
        .form-group textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 4px;
            font-family: 'Lato', sans-serif;
        }

        .form-group input:focus, 
        .form-group select:focus, 
        .form-group textarea:focus {
            border-color: var(--primary-maroon);
            outline: none;
        }

        /* --- Footer --- */
        footer {
            background-color: var(--primary-maroon);
            color: white;
            padding: 3rem 2rem;
            margin-top: auto;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
        }

        .footer-col h3 {
            color: white;
            margin-bottom: 1rem;
            font-size: 1.2rem;
        }

        .footer-col ul li {
            margin-bottom: 0.5rem;
        }

        .footer-col ul li a {
            color: #ddd;
        }

        .footer-col ul li a:hover {
            color: white;
        }

        .social-icons a {
            color: white;
            font-size: 1.2rem;
            margin-right: 15px;
        }

        .copyright {
            text-align: center;
            margin-top: 2rem;
            padding-top: 1rem;
            border-top: 1px solid rgba(255,255,255,0.1);
            font-size: 0.9rem;
            color: #ddd;
        }

        /* --- Responsive Design --- */
        @media (max-width: 768px) {
            .navbar {
                flex-direction: column;
                gap: 1rem;
            }
            
            .nav-links {
                flex-wrap: wrap;
                justify-content: center;
                gap: 1rem;
            }

            .hero-content h1 {
                font-size: 2.5rem;
            }
        }
    </style>
</head>
<body>

    <!-- Header Section -->
    <header>
        <div class="navbar">
            <div class="logo">Velvet & Silk</div>
            <nav>
                <ul class="nav-links">
                    <li><a href="#">Home</a></li>
                    <li><a href="#products">Shop</a></li>
                    <li><a href="#categories">Categories</a></li>
                    <li><a href="#">New Arrivals</a></li>
                    <li><a href="#">Offers</a></li>
                    <li><a href="#admin">Contact</a></li>
                </ul>
            </nav>
            <div class="search-bar">
                <input type="text" placeholder="Search sarees...">
                <button><i class="fas fa-search"></i></button>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h1>Grace in Every Drape</h1>
            <p>Experience the timeless elegance of Indian craftsmanship</p>
            <a href="#products" class="btn">Shop Now</a>
        </div>
    </section>

    <!-- Categories Dropdown -->
    <section id="categories" class="category-section">
        <div class="category-container">
            <button class="category-btn">Browse Collections <i class="fas fa-chevron-down"></i></button>
            <div class="dropdown-content">
                <a href="#">Silk Sarees</a>
                <a href="#">Cotton Sarees</a>
                <a href="#">Banarasi Sarees</a>
                <a href="#">Designer Sarees</a>
                <a href="#">Wedding Collection</a>
            </div>
        </div>
    </section>

    <!-- Product Section -->
    <section id="products" class="products-section">
        <h2 class="section-title">New Arrivals</h2>
        <div class="product-grid">
            <!-- Product 1 -->
            <div class="product-card">
                <img src="https://images.unsplash.com/photo-1617627143750-d86bc21e42bb?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="Red Silk Saree" class="product-image">
                <div class="product-info">
                    <h3 class="product-name">Royal Maroon Banarasi</h3>
                    <p class="product-price">$120.00</p>
                    <div class="card-buttons">
                        <button class="btn" onclick="addToCart('Royal Maroon Banarasi')">Add to Cart</button>
                        <button class="btn-outline">View Details</button>
                    </div>
                </div>
            </div>

            <!-- Product 2 -->
            <div class="product-card">
                <img src="https://images.unsplash.com/photo-1583391733958-e04e9c760997?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="Gold Kanjivaram" class="product-image">
                <div class="product-info">
                    <h3 class="product-name">Golden Kanjivaram</h3>
                    <p class="product-price">$250.00</p>
                    <div class="card-buttons">
                        <button class="btn" onclick="addToCart('Golden Kanjivaram')">Add to Cart</button>
                        <button class="btn-outline">View Details</button>
                    </div>
                </div>
            </div>

            <!-- Product 3 -->
            <div class="product-card">
                <img src="https://images.unsplash.com/photo-1610189012906-4783382c50
