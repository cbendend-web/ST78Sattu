# ST78Sattu
Create a website for my Business 
<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ST78 Sattu - Pure & Natural Sattu | Free Home Delivery</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
        }

        /* Header */
        header {
            background: linear-gradient(135deg, #8B4513, #D2691E);
            color: white;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        .logo {
            font-size: 2rem;
            font-weight: bold;
            color: #FFD700;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: #FFD700;
        }

        .order-btn {
            background: #FFD700;
            color: #8B4513;
            padding: 0.8rem 2rem;
            border-radius: 25px;
            text-decoration: none;
            font-weight: bold;
            transition: transform 0.3s;
        }

        .order-btn:hover {
            transform: scale(1.05);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(139,69,19,0.8), rgba(210,105,30,0.8)), 
                        url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 600"><rect fill="%23f5f5dc" width="1200" height="600"/><circle fill="%23d2b48c" cx="200" cy="200" r="100"/><circle fill="%23deb887" cx="800" cy="300" r="150"/><circle fill="%23f4a460" cx="1000" cy="150" r="80"/></svg>');
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            margin-top: 80px;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }

        .hero-content p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
        }

        /* Products Section */
        .products {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #8B4513;
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .product-card {
            background: white;
            border-radius: 15px;
            padding: 2rem;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.2);
        }

        .product-img {
            width: 120px;
            height: 120px;
            background: linear-gradient(45deg, #D2691E, #DEB887);
            border-radius: 50%;
            margin: 0 auto 1rem;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
            color: white;
        }

        .product-price {
            font-size: 2rem;
            color: #8B4513;
            font-weight: bold;
            margin: 1rem 0;
        }

        /* Order Section */
        .order-section {
            background: linear-gradient(135deg, #FFD700, #FFA500);
            padding: 5rem 2rem;
            text-align: center;
            color: #8B4513;
        }

        .order-form {
            max-width: 500px;
            margin: 2rem auto;
            background: white;
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: bold;
        }

        .form-group input, .form-group select {
            width: 100%;
            padding: 1rem;
            border: 2px solid #ddd;
            border-radius: 10px;
            font-size: 1rem;
        }

        .submit-btn {
            background: #8B4513;
            color: white;
            padding: 1rem 3rem;
            border: none;
            border-radius: 25px;
            font-size: 1.2rem;
            cursor: pointer;
            transition: background 0.3s;
            width: 100%;
        }

        .submit-btn:hover {
            background: #A0522D;
        }

        /* Features */
        .features {
            padding: 5rem 2rem;
            background: #f8f8f8;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            max-width: 1200px;
            margin: 3rem auto 0;
        }

        .feature {
            text-align: center;
            padding: 2rem;
        }

        .feature i {
            font-size: 3rem;
            color: #D2691E;
            margin-bottom: 1rem;
        }

        /* Footer */
        footer {
            background: #333;
            color: white;
            text-align: center;
            padding: 2rem;
        }

        .contact-info {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-bottom: 1rem;
            flex-wrap: wrap;
        }

        /* Mobile Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero-content h1 {
                font-size: 2.5rem;
            }
            
            .logo {
                font-size: 1.5rem;
            }
        }

        /* WhatsApp Button */
        .whatsapp-float {
            position: fixed;
            width: 60px;
            height: 60px;
            bottom: 40px;
            right: 40px;
            background-color: #25d366;
            color: #FFF;
            border-radius: 50px;
            text-align: center;
            font-size: 30px;
            box-shadow: 2px 2px 3px #999;
            z-index: 100;
            animation: whatsapp-bounce 2s infinite;
        }

        @keyframes whatsapp-bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
            40% { transform: translateY(-10px); }
            60% { transform: translateY(-5px); }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <nav>
            <div class="logo">ST78 Sattu</div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#products">Products</a></li>
                <li><a href="#order">Order Now</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <a href="#order" class="order-btn">Order Now</a>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h1>ST78 Sattu</h1>
            <p>100% Pure & Natural Sattu<br>Free Home Delivery | Fresh & Healthy</p>
            <a href="#order" class="order-btn" style="font-size: 1.3rem; padding: 1rem 3rem;">Order Now - Free Delivery</a>
        </div>
    </section>

    <!-- Products Section -->
    <section id="products" class="products">
        <h2 class="section-title">Our Premium Sattu Products</h2>
        <div class="products-grid">
            <div class="product-card">
                <div class="product-img">
                    <i class="fas fa-seedling"></i>
                </div>
                <h3>Classic Sattu</h3>
                <p>100% Pure Roasted Gram Flour</p>
                <div class="product-price">₹99/kg</div>
                <button class="submit-btn" onclick="addToCart('Classic Sattu', 99)">Add to Cart</button>
            </div>
            <div class="product-card">
                <div class="product-img">
                    <i class="fas fa-lemon"></i>
                </div>
                <h3>Gur Wala Sattu</h3>
                <p>Sattu with Pure Jaggery</p>
                <div class="product-price">₹129/kg</div>
                <button class="submit-btn" onclick="addToCart('Gur Wala Sattu', 129)">Add to Cart</button>
            </div>
            <div class="product-card">
                <div class="product-img">
                    <i class="fas fa-star"></i>
                </div>
                <h3>Premium Sattu</h3>
                <p>Finest Quality with Dry Fruits</p>
                <div class="product-price">₹179/kg</div>
                <button class="submit-btn" onclick="addToCart('Premium Sattu', 179)">Add to Cart</button>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="features">
        <h2 class="section-title">Why Choose ST78 Sattu?</h2>
        <div class="features-grid">
            <div class="feature">
                <i class="fas fa-truck"></i>
                <h3>Free Delivery</h3>
                <p>Free home delivery anywhere in your city</p>
            </div>
            <div class="feature">
                <i class="fas fa-leaf"></i>
                <h3>100% Natural</h3>
                <p>No preservatives, pure & organic</p>
            </div>
            <div class="feature">
                <i class="fas fa-shield-alt"></i>
                <h3>Fresh Guaranteed</h3>
                <p>Freshly roasted every week</p>
            </div>
            <div class="feature">
                <i class="fas fa-clock"></i>
                <h3>Fast Delivery</h3>
                <p>Order today, get tomorrow</p>
            </div>
        </div>
    </section>

    <!-- Order Section -->
    <section id="order" class="order-section">
        <h2 class="section-title">Quick Order - Free Delivery</h2>
        <form class="order-form" onsubmit="placeOrder(event)">
            <div class="form-group">
                <label><i class="fas fa-user"></i> Full Name</label>
                <input type="text" id="name" required>
            </div>
            <div class="form-group">
                <label><i class="fas fa-phone"></i> Phone Number</label>
                <input type="tel" id="phone" required>
            </div>
            <div class="form-group">
                <label><i class="fas fa-map-marker-alt"></i> Delivery Address</label>
                <textarea id="address" rows="3" required></textarea>
            </div>
            <div class="form-group">
                <label><i class="fas fa-shopping-cart"></i> Products & Quantity</label>
                <textarea id="products" rows="3" placeholder="Example: Classic Sattu - 2kg, Gur Wala - 1kg" required></textarea>
            </div>
            <button type="submit" class="submit-btn">
                <i class="fas fa-check"></i> Place Order Now
            </button>
        </form>
    </section>

    <!-- WhatsApp Float Button -->
    <a href="https://wa.me/91YOURNUMBER?text=Hi%2C%20I%20want%20to%20order%20ST78%20Sattu" class="whatsapp-float" target="_blank">
        <i class="fab fa-whatsapp"></i>
    </a>

    <!-- Footer -->
    <footer id="contact">
        <div class="contact-info">
            <div><i class="fas fa-phone"></i> +91 98XXX XXXXX</div>
            <div><i class="fas fa-envelope"></i> st78sattu@gmail.com</div>
            <div><i class="fas fa-clock"></i> 24x7 Support</div>
        </div>
        <p>&copy; 2024 ST78 Sattu. All rights reserved. | Pure & Natural Sattu</p>
    </footer>

    <script>
        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Cart functionality
        let cart = [];
        function addToCart(product, price) {
            cart.push({product, price});
            alert(`${product} added to cart!`);
        }

        // Order form submission
        function placeOrder(event) {
            event.preventDefault();
            
            const name = document.getElementById('name').value;
            const phone = document.getElementById('phone').value;
            const address = document.getElementById('address').value;
            const products = document.getElementById('products').value;

            // WhatsApp order message
            const message = `New Order from ST78 Sattu Website!%0A%0AName: ${name}%0APhone: ${phone}%0AAddress: ${address}%0AProducts: ${products}`;
            
            const whatsappUrl = `https://wa.me/91YOURPHONENUMBER?text=${message}`;
            window.open(whatsappUrl, '_blank');
            
            alert('Order placed successfully! You will receive a WhatsApp confirmation.');
            document.querySelector('.order-form').reset();
        }

        // Auto-scroll to order section on load if URL has #order
        if (window.location.hash === '#order') {
            setTimeout(() => {
                document.querySelector('#order').scrollIntoView({behavior: 'smooth'});
            }, 500);
        }
    </script>
</body>
</html>
