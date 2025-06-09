<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>آکادمی بوکس قلعه | آموزش حرفه‌ای بوکس</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            -webkit-tap-highlight-color: transparent;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #ffffff;
            color: #000000;
            line-height: 1.6;
            overflow-x: hidden;
            touch-action: pan-y;
        }
        
        /* Header Styles */
        header {
            background-color: #ffffff;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 100;
            padding: 5px 0;
        }
        
        .logo-container {
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 5px;
        }
        
        .logo {
            width: 60px;
            height: 60px;
            background-color: #f5f5f5;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            margin: 0 auto;
            border: 2px solid #000;
            overflow: hidden;
        }
        
        .logo img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .club-name {
            text-align: center;
            font-size: 18px;
            font-weight: bold;
            margin-top: 5px;
            color: #000;
            text-shadow: 0 1px 2px rgba(0,0,0,0.1);
        }
        
        /* Main Content */
        .section-title {
            text-align: center;
            font-size: 20px;
            margin: 15px 0 12px;
            padding-bottom: 8px;
            border-bottom: 2px solid #000;
            position: relative;
            color: #000;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -2px;
            left: 50%;
            transform: translateX(-50%);
            width: 60px;
            height: 2px;
            background: #e53935;
        }
        
        /* Shop Section */
        .shop {
            padding: 12px;
            background-color: #fff;
        }
        
        .products {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(140px, 1fr));
            gap: 12px;
            margin-top: 12px;
        }
        
        .product {
            background: #fff;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 3px 6px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
            border: 1px solid #eee;
        }
        
        .product:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
        }
        
        .product-img {
            width: 100%;
            height: 120px;
            background-color: #f9f9f9;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .product-img img {
            max-width: 100%;
            max-height: 100%;
            object-fit: cover;
        }
        
        .product-info {
            padding: 10px;
        }
        
        .product-title {
            font-size: 14px;
            font-weight: 600;
            margin-bottom: 5px;
            color: #000;
            height: 40px;
            overflow: hidden;
        }
        
        .product-price {
            font-size: 16px;
            font-weight: bold;
            color: #e53935;
            margin-bottom: 8px;
        }
        
        .order-btn {
            display: block;
            width: 100%;
            padding: 7px;
            background-color: #25D366;
            color: white;
            border: none;
            border-radius: 4px;
            font-weight: bold;
            cursor: pointer;
            text-align: center;
            text-decoration: none;
            font-size: 13px;
        }
        
        /* Gallery Section */
        .gallery {
            padding: 12px;
            background-color: #f8f8f8;
        }
        
        .photos {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
            gap: 8px;
            margin-top: 12px;
        }
        
        .photo {
            width: 100%;
            height: 100px;
            background-color: #eee;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }
        
        .photo img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.3s ease;
        }
        
        .photo:hover img {
            transform: scale(1.05);
        }
        
        /* Ads Section */
        .ads {
            padding: 12px;
            background-color: #fff;
        }
        
        .ad-container {
            background-color: #f9f9f9;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 3px 6px rgba(0, 0, 0, 0.1);
            margin-top: 12px;
            border: 1px solid #eee;
        }
        
        .ad-img {
            width: 100%;
            height: 140px;
            background-color: #e0e0e0;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .ad-img img {
            max-width: 100%;
            max-height: 100%;
            object-fit: cover;
        }
        
        .ad-content {
            padding: 10px;
            text-align: center;
        }
        
        .ad-title {
            font-size: 16px;
            font-weight: bold;
            margin-bottom: 5px;
            color: #000;
        }
        
        .ad-text {
            font-size: 13px;
            color: #555;
        }
        
        /* Contact Section */
        .contact {
            padding: 12px;
            background-color: #f8f8f8;
        }
        
        .contact-info {
            margin-top: 12px;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 10px;
            padding: 8px;
            background: #fff;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
        }
        
        .contact-icon {
            width: 34px;
            height: 34px;
            background-color: #000;
            color: #fff;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-left: 8px;
            flex-shrink: 0;
        }
        
        .contact-details {
            flex: 1;
        }
        
        .contact-title {
            font-weight: bold;
            font-size: 14px;
            margin-bottom: 3px;
            color: #000;
        }
        
        .contact-text {
            font-size: 13px;
            color: #555;
        }
        
        .map {
            width: 100%;
            height: 200px;
            background-color: #e9e9e9;
            border-radius: 8px;
            overflow: hidden;
            margin-top: 12px;
            box-shadow: 0 3px 6px rgba(0, 0, 0, 0.1);
        }
        
        /* Social Media */
        .social-media {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin-top: 18px;
            padding: 12px 0;
        }
        
        .social-icon {
            width: 42px;
            height: 42px;
            border-radius: 50%;
            background-color: #000;
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 18px;
            text-decoration: none;
            transition: transform 0.3s ease, background-color 0.3s ease;
            box-shadow: 0 3px 5px rgba(0, 0, 0, 0.1);
        }
        
        .social-icon:hover {
            transform: translateY(-3px);
        }
        
        .whatsapp { background-color: #25D366; }
        .telegram { background-color: #0088cc; }
        .instagram { background-color: #E1306C; }
        .rubika { background-color: #00A4E0; }
        
        /* Footer */
        footer {
            background-color: #000;
            color: #fff;
            text-align: center;
            padding: 12px;
            font-size: 12px;
        }
        
        .copyright {
            margin-top: 6px;
            color: #aaa;
        }
        
        /* Responsive Design */
        @media (max-width: 480px) {
            .logo {
                width: 55px;
                height: 55px;
            }
            
            .club-name {
                font-size: 16px;
            }
            
            .section-title {
                font-size: 18px;
            }
            
            .products {
                grid-template-columns: repeat(auto-fill, minmax(130px, 1fr));
                gap: 10px;
            }
            
            .product-img {
                height: 110px;
            }
            
            .photos {
                grid-template-columns: repeat(auto-fill, minmax(90px, 1fr));
            }
        }
        
        @media (max-width: 360px) {
            .products {
                grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
            }
            
            .logo {
                width: 50px;
                height: 50px;
            }
            
            .club-name {
                font-size: 15px;
            }
        }
        
        /* Disable zooming */
        body {
            touch-action: pan-y;
            -webkit-user-scalable: no;
            user-scalable: no;
        }
        
        input, textarea {
            font-size: 16px;
        }
        
        /* Smooth scrolling for touch devices */
        html {
            scroll-behavior: smooth;
            -webkit-overflow-scrolling: touch;
        }
    </style>
</head>
<body>
    <!-- Header with Logo -->
    <header>
        <div class="logo-container">
            <div class="logo">
                <!-- لوگوی کوچک در بالای صفحه -->
                <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'%3E%3Ccircle cx='50' cy='50' r='48' stroke='black' stroke-width='2' fill='white'/%3E%3Cpath d='M30,30 L70,70 M70,30 L30,70' stroke='black' stroke-width='3'/%3E%3C/svg%3E" alt="لوگوی آکادمی بوکس قلعه">
            </div>
        </div>
        <div class="club-name">آکادمی بوکس قلعه</div>
    </header>

    <!-- Shop Section -->
    <section class="shop">
        <h2 class="section-title">فروشگاه لوازم ورزشی</h2>
        <div class="products">
            <div class="product">
                <div class="product-img">
                    <img src="https://images.unsplash.com/photo-1591117207239-788bf8de6c3b?auto=format&fit=crop&q=80&w=500" alt="دستکش بوکس">
                </div>
                <div class="product-info">
                    <h3 class="product-title">دستکش بوکس حرفه‌ای</h3>
                    <div class="product-price">1,290,000 تومان</div>
                    <a href="https://wa.me/989123456789?text=سلام، می‌خوام دستکش بوکس حرفه‌ای سفارش بدم" class="order-btn">سفارش در واتساپ</a>
                </div>
            </div>
            
            <div class="product">
                <div class="product-img">
                    <img src="https://images.unsplash.com/photo-1541534741688-6078c6bfb5c5?auto=format&fit=crop&q=80&w=500" alt="کمربند محافظ">
                </div>
                <div class="product-info">
                    <h3 class="product-title">کمربند محافظ بوکس</h3>
                    <div class="product-price">650,000 تومان</div>
                    <a href="https://wa.me/989123456789?text=سلام، می‌خوام کمربند محافظ بوکس سفارش بدم" class="order-btn">سفارش در واتساپ</a>
                </div>
            </div>
            
            <div class="product">
                <div class="product-img">
                    <img src="https://images.unsplash.com/photo-1551983087-5b5c935d0d7a?auto=format&fit=crop&q=80&w=500" alt="لباس ورزشی">
                </div>
                <div class="product-info">
                    <h3 class="product-title">ست لباس ورزشی</h3>
                    <div class="product-price">890,000 تومان</div>
                    <a href="https://wa.me/989123456789?text=سلام، می‌خوام ست لباس ورزشی سفارش بدم" class="order-btn">سفارش در واتساپ</a>
                </div>
            </div>
            
            <div class="product">
                <div class="product-img">
                    <img src="https://images.unsplash.com/photo-1543163521-1bf539c55dd2?auto=format&fit=crop&q=80&w=500" alt="کفش بوکس">
                </div>
                <div class="product-info">
                    <h3 class="product-title">کفش بوکس حرفه‌ای</h3>
                    <div class="product-price">1,550,000 تومان</div>
                    <a href="https://wa.me/989123456789?text=سلام، می‌خوام کفش بوکس حرفه‌ای سفارش بدم" class="order-btn">سفارش در واتساپ</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Gallery Section -->
    <section class="gallery">
        <h2 class="section-title">گالری تصاویر</h2>
        <div class="photos">
            <div class="photo">
                <img src="https://images.unsplash.com/photo-1518611012118-696072aa579a?auto=format&fit=crop&q=80&w=500" alt="تمرین">
            </div>
            <div class="photo">
                <img src="https://images.unsplash.com/photo-1571019613454-1cb2f99b2d8b?auto=format&fit=crop&q=80&w=500" alt="مسابقه">
            </div>
            <div class="photo">
                <img src="https://images.unsplash.com/photo-1599058917212-d750089bc07e?auto=format&fit=crop&q=80&w=500" alt="تیم">
            </div>
            <div class="photo">
                <img src="https://images.unsplash.com/photo-1534258936925-c58bed479fcb?auto=format&fit=crop&q=80&w=500" alt="سالن">
            </div>
            <div class="photo">
                <img src="https://images.unsplash.com/photo-1533681470484-bf8e7270d0a6?auto=format&fit=crop&q=80&w=500" alt="تمرین">
            </div>
            <div class="photo">
                <img src="https://images.unsplash.com/photo-1517836357463-d25dfeac3438?auto=format&fit=crop&q=80&w=500" alt="مسابقه">
            </div>
            <div class="photo">
                <img src="https://images.unsplash.com/photo-1571019614242-c5c5dee9f50b?auto=format&fit=crop&q=80&w=500" alt="مربی">
            </div>
            <div class="photo">
                <img src="https://images.unsplash.com/photo-1518611012118-696072aa579a?auto=format&fit=crop&q=80&w=500" alt="ورزشکاران">
            </div>
        </div>
    </section>

    <!-- Ads Section -->
    <section class="ads">
        <h2 class="section-title">تبلیغات</h2>
        <div class="ad-container">
            <div class="ad-img">
                <img src="https://images.unsplash.com/photo-1517344884509-a0c97ec11bcc?auto=format&fit=crop&q=80&w=1000" alt="تبلیغات">
            </div>
            <div class="ad-content">
                <h3 class="ad-title">دوره تابستانه بوکس</h3>
                <p class="ad-text">ثبت نام دوره تابستانه با 20% تخفیف ویژه شروع شد. ظرفیت محدود!</p>
            </div>
        </div>
        
        <div class="ad-container" style="margin-top: 15px;">
            <div class="ad-img">
                <img src="https://images.unsplash.com/photo-1593079831268-3381b0db4a77?auto=format&fit=crop&q=80&w=1000" alt="تبلیغات">
            </div>
            <div class="ad-content">
                <h3 class="ad-title">مسابقات قهرمانی</h3>
                <p class="ad-text">شرکت در مسابقات قهرمانی استان تهران - آماده‌سازی حرفه‌ای</p>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact">
        <h2 class="section-title">تماس با ما</h2>
        <div class="contact-info">
            <div class="contact-item">
                <div class="contact-icon">
                    <i class="fas fa-map-marker-alt"></i>
                </div>
                <div class="contact-details">
                    <div class="contact-title">آدرس</div>
                    <div class="contact-text">تهران، خیابان آزادی، کوچه بوکس، پلاک 12</div>
                </div>
            </div>
            
            <div class="contact-item">
                <div class="contact-icon">
                    <i class="fas fa-phone"></i>
                </div>
                <div class="contact-details">
                    <div class="contact-title">تلفن</div>
                    <div class="contact-text">021-12345678 | 09123456789</div>
                </div>
            </div>
            
            <div class="contact-item">
                <div class="contact-icon">
                    <i class="fas fa-clock"></i>
                </div>
                <div class="contact-details">
                    <div class="contact-title">ساعات کاری</div>
                    <div class="contact-text">شنبه تا پنجشنبه: 8 صبح تا 10 شب</div>
                </div>
            </div>
        </div>
        
        <div class="map">
            <!-- نقشه گوگل -->
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3239.6793032261077!2d51.38827731526948!3d35.73248898018761!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zMzXCsDQzJzU2LjkiTiA1McKwMjMnMjIuOSJF!5e0!3m2!1sen!2s!4v1651234567890!5m2!1sen!2s" 
                    width="100%" 
                    height="100%" 
                    style="border:0;" 
                    allowfullscreen="" 
                    loading="lazy"></iframe>
        </div>
    </section>

    <!-- Social Media -->
    <div class="social-media">
        <a href="https://t.me/boxingghale" class="social-icon telegram">
            <i class="fab fa-telegram"></i>
        </a>
        <a href="https://wa.me/989123456789" class="social-icon whatsapp">
            <i class="fab fa-whatsapp"></i>
        </a>
        <a href="https://rubika.ir/boxingghale" class="social-icon rubika">
            <i class="fas fa-comment-dots"></i>
        </a>
        <a href="https://instagram.com/boxingghale" class="social-icon instagram">
            <i class="fab fa-instagram"></i>
        </a>
    </div>

    <!-- Footer -->
    <footer>
        <div>آکادمی بوکس قلعه</div>
        <div class="copyright">© 2023 تمامی حقوق محفوظ است</div>
    </footer>

    <script>
        // Disable zooming with double-tap
        document.addEventListener('dblclick', function(e) {
            e.preventDefault();
        }, { passive: false });
        
        // Prevent context menu on long press
        document.addEventListener('contextmenu', function(e) {
            e.preventDefault();
        });
        
        // Enable smooth scrolling for touch devices
        document.addEventListener('touchstart', function() {}, {passive: true});
        document.addEventListener('touchmove', function() {}, {passive: true});
    </script>
</body>
</html>
