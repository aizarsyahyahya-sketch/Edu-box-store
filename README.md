```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Berkah Abadi - Toko Serba Ada Bekasi</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        :root {
            --primary: #2c3e50;
            --secondary: #3498db;
            --accent: #e74c3c;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --success: #27ae60;
        }
        
        body {
            background-color: #f9f9f9;
            color: #333;
            line-height: 1.6;
        }
        
        /* Header & Navigation */
        header {
            background: linear-gradient(135deg, var(--primary) 0%, #1a252f 100%);
            color: white;
            padding: 1rem 0;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .logo i {
            font-size: 2.5rem;
            color: var(--secondary);
        }
        
        .logo h1 {
            font-size: 1.8rem;
            font-weight: 700;
        }
        
        .logo p {
            font-size: 0.9rem;
            opacity: 0.8;
        }
        
        nav ul {
            display: flex;
            list-style: none;
            gap: 25px;
        }
        
        nav a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            font-size: 1.1rem;
            transition: color 0.3s;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        nav a:hover {
            color: var(--secondary);
        }
        
        .mobile-menu {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(44, 62, 80, 0.9), rgba(44, 62, 80, 0.9)), 
                        url('https://images.unsplash.com/photo-1556742049-0cfed4f6a45d?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 5rem 0;
            text-align: center;
        }
        
        .hero h2 {
            font-size: 3rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 2rem;
            opacity: 0.9;
        }
        
        .cta-button {
            display: inline-block;
            background-color: var(--accent);
            color: white;
            padding: 15px 40px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.1rem;
            transition: all 0.3s;
            box-shadow: 0 5px 15px rgba(231, 76, 60, 0.4);
        }
        
        .cta-button:hover {
            background-color: #c0392b;
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(231, 76, 60, 0.6);
        }
        
        /* Products Section */
        .section-title {
            text-align: center;
            margin: 3rem 0 2rem;
            color: var(--primary);
            font-size: 2.5rem;
            position: relative;
        }
        
        .section-title:after {
            content: '';
            display: block;
            width: 100px;
            height: 4px;
            background: var(--secondary);
            margin: 10px auto;
            border-radius: 2px;
        }
        
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 30px;
            margin-bottom: 4rem;
        }
        
        .product-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.15);
        }
        
        .product-img {
            height: 200px;
            background-color: #f5f5f5;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
            color: var(--primary);
        }
        
        .product-info {
            padding: 20px;
        }
        
        .product-category {
            color: var(--secondary);
            font-size: 0.9rem;
            font-weight: 600;
            text-transform: uppercase;
            margin-bottom: 5px;
        }
        
        .product-name {
            font-size: 1.3rem;
            margin-bottom: 10px;
            color: var(--dark);
        }
        
        .product-price {
            color: var(--accent);
            font-size: 1.4rem;
            font-weight: 700;
            margin-bottom: 15px;
        }
        
        /* Store Info */
        .store-info {
            background-color: white;
            border-radius: 10px;
            padding: 30px;
            margin: 3rem 0;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }
        
        .info-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 30px;
        }
        
        .info-item {
            display: flex;
            align-items: flex-start;
            gap: 15px;
        }
        
        .info-icon {
            background-color: var(--secondary);
            color: white;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.3rem;
            flex-shrink: 0;
        }
        
        /* Map */
        .map-container {
            margin: 4rem 0;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            height: 400px;
        }
        
        .map-container iframe {
            width: 100%;
            height: 100%;
            border: none;
        }
        
        /* Contact */
        .contact-form {
            background-color: white;
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            margin-bottom: 4rem;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: var(--dark);
        }
        
        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            transition: border 0.3s;
        }
        
        .form-control:focus {
            border-color: var(--secondary);
            outline: none;
        }
        
        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }
        
        .submit-btn {
            background-color: var(--success);
            color: white;
            border: none;
            padding: 15px 40px;
            border-radius: 5px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        
        .submit-btn:hover {
            background-color: #219653;
        }
        
        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 3rem 0 1.5rem;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 2rem;
        }
        
        .footer-logo h3 {
            font-size: 1.8rem;
            margin-bottom: 10px;
            color: var(--secondary);
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-links a {
            color: white;
            background-color: rgba(255,255,255,0.1);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s;
            text-decoration: none;
        }
        
        .social-links a:hover {
            background-color: var(--secondary);
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 1.5rem;
            border-top: 1px solid rgba(255,255,255,0.1);
            font-size: 0.9rem;
            opacity: 0.8;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .mobile-menu {
                display: block;
            }
            
            nav ul {
                display: none;
                width: 100%;
                flex-direction: column;
                gap: 0;
                margin-top: 20px;
            }
            
            nav ul.active {
                display: flex;
            }
            
            nav li {
                border-bottom: 1px solid rgba(255,255,255,0.1);
            }
            
            nav a {
                padding: 15px 0;
            }
            
            .hero h2 {
                font-size: 2.2rem;
            }
            
            .section-title {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-content">
            <div class="logo">
                <i class="fas fa-store"></i>
                <div>
                    <h1>Berkah Abadi</h1>
                    <p>Toko Serba Ada Bekasi</p>
                </div>
            </div>
            
            <div class="mobile-menu" id="mobileMenu">
                <i class="fas fa-bars"></i>
            </div>
            
            <nav>
                <ul id="navMenu">
                    <li><a href="#home"><i class="fas fa-home"></i> Beranda</a></li>
                    <li><a href="#products"><i class="fas fa-box-open"></i> Produk</a></li>
                    <li><a href="#info"><i class="fas fa-info-circle"></i> Info Toko</a></li>
                    <li><a href="#location"><i class="fas fa-map-marker-alt"></i> Lokasi</a></li>
                    <li><a href="#contact"><i class="fas fa-envelope"></i> Kontak</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <h2>Selamat Datang di Toko Berkah Abadi</h2>
            <p>Toko serba ada terlengkap di Bekasi dengan harga terjangkau dan kualitas terjamin. Melayani dengan ramah dan profesional sejak 2010.</p>
            <a href="#products" class="cta-button">Lihat Produk Kami <i class="fas fa-arrow-right"></i></a>
        </div>
    </section>

    <!-- Products Section -->
    <section class="container" id="products">
        <h2 class="section-title">Produk Unggulan</h2>
        <div class="products-grid">
            <!-- Product 1 -->
            <div class="product-card">
                <div class="product-img" style="background-color: #fff8e1;">
                    <i class="fas fa-utensils"></i>
                </div>
                <div class="product-info">
                    <div class="product-category">Perlengkapan Dapur</div>
                    <h3 class="product-name">Paket Alat Masak Lengkap</h3>
                    <div class="product-price">Rp 350.000</div>
                    <p>Set alat masak berkualitas dengan 15 item lengkap untuk kebutuhan dapur Anda.</p>
                </div>
            </div>
            
            <!-- Product 2 -->
            <div class="product-card">
                <div class="product-img" style="background-color: #e8f5e9;">
                    <i class="fas fa-broom"></i>
                </div>
                <div class="product-info">
                    <div class="product-category">Kebersihan</div>
                    <h3 class="product-name">Paket Alat Kebersihan</h3>
                    <div class="product-price">Rp 185.000</div>
                    <p>Sapu, pel, kemoceng, dan cairan pembersih lantai dengan kualitas terbaik.</p>
                </div>
            </div>
            
            <!-- Product 3 -->
            <div class="product-card">
                <div class="product-img" style="background-color: #e3f2fd;">
                    <i class="fas fa-lightbulb"></i>
                </div>
                <div class="product-info">
                    <div class="product-category">Elektronik</div>
                    <h3 class="product-name">Lampu LED Hemat Energi</h3>
                    <div class="product-price">Rp 25.000</div>
                    <p>Lampu LED 10W setara 75W, hemat listrik, umur panjang, garansi 1 tahun.</p>
                </div>
            </div>
            
            <!-- Product 4 -->
            <div class="product-card">
                <div class="product-img" style="background-color: #f3e5f5;">
                    <i class="fas fa-toolbox"></i>
                </div>
                <div class="product-info">
                    <div class="product-category">Perkakas</div>
                    <h3 class="product-name">Toolkit Perkakas Rumah</h3>
                    <div class="product-price">Rp 275.000</div>
                    <p>Perkakas lengkap 32-in-1 untuk perbaikan rumah tangga, kualitas industri.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Store Info -->
    <section class="container" id="info">
        <h2 class="section-title">Informasi Toko</h2>
        <div class="store-info">
            <p><strong>Toko Berkah Abadi</strong> telah melayani masyarakat Bekasi dan sekitarnya sejak tahun 2010. Kami menyediakan berbagai kebutuhan rumah tangga, elektronik, perkakas, dan perlengkapan sehari-hari dengan harga kompetitif dan kualitas terjamin.</p>
            
            <div class="info-grid">
                <div class="info-item">
                    <div class="info-icon">
                        <i class="fas fa-clock"></i>
                    </div>
                    <div>
                        <h3>Jam Operasional</h3>
                        <p>Senin - Minggu: 08:00 - 21:00 WIB</p>
                        <p>Hari Libur: Tetap Buka</p>
                    </div>
                </div>
                
                <div class="info-item">
                    <div class="info-icon">
                        <i class="fas fa-phone"></i>
                    </div>
                    <div>
                        <h3>Kontak</h3>
                        <p>Telepon: (021) 8895-6734</p>
                        <p>WhatsApp: 0812-3456-7890</p>
                    </div>
                </div>
                
                <div class="info-item">
                    <div class="info-icon">
                        <i class="fas fa-truck"></i>
                    </div>
                    <div>
                        <h3>Layanan</h3>
                        <p>Gratis ongkir wilayah Bekasi (min. Rp 200.000)</p>
                        <p>Pesan antar melalui WhatsApp</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Location Map -->
    <section class="container" id="location">
        <h2 class="section-title">Lokasi Toko</h2>
        <div class="map-container">
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3966.123456789012!2d106.9891234!3d-6.2345678!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zNsKwMTQnMDQuNCJTIDEwNsKwNTknMjguOCJF!5e0!3m2!1sid!2sid!4v1234567890123!5m2!1sid!2sid" 
                    allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade">
            </iframe>
        </div>
        <div style="text-align: center; margin-top: 20px;">
            <p><strong>Alamat:</strong> Jl. Raya Bekasi KM 25, No. 123, Bekasi Timur, Jawa Barat 17111</p>
            <a href="https://maps.app.goo.gl/Md8SRTboqiunRmG56" target="_blank" class="cta-button" style="padding: 10px 25px; font-size: 1rem;">
                <i class="fas fa-map-marked-alt"></i> Buka di Google Maps
            </a>
        </div>
    </section>

    <!-- Contact Form -->
    <section class="container" id="contact">
        <h2 class="section-title">Hubungi Kami</h2>
        <div class="contact-form">
            <form id="contactForm">
                <div class="form-group">
                    <label for="name">Nama Lengkap</label>
                    <input type="text" id="name" class="form-control" placeholder="Masukkan nama Anda" required>
                </div>
                
                <div class="form-group">
                    <label for="phone">Nomor WhatsApp</label>
                    <input type="tel" id="phone" class="form-control" placeholder="Contoh: 081234567890" required>
                </div>
                
                <div class="form-group">
                    <label for="message">Pesan</label>
                    <textarea id="message" class="form-control" placeholder="Tulis pesan Anda di sini..." required></textarea>
                </div>
                
                <button type="submit" class="submit-btn">
                    <i class="fas fa-paper-plane"></i> Kirim Pesan
                </button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-logo">
                    <h3>Berkah Abadi</h3>
                    <p>Toko Serba Ada Bekasi</p>
                    <p>Melayani dengan hati sejak 2010</p>
                    
                    <div class="social-links">
                        <a href="#"><i class="fab fa-whatsapp"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-facebook"></i></a>
                        <a href="#"><i class="fab fa-tiktok"></i></a>
                    </div>
                </div>
                
                <div>
                    <h4>Layanan</h4>
                    <ul style="list-style: none; margin-top: 15px;">
                        <li><a href="#" style="color: #ddd; text-decoration: none;">Pesan Antar</a></li>
                        <li><a href="#" style="color: #ddd; text-decoration: none;">Grosir & Partai</a></li>
                        <li><a href="#" style="color: #ddd; text-decoration: none;">Garansi Produk</a></li>
                        <li><a href="#" style="color: #ddd; text-decoration: none;">Pembayaran COD</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4>Kontak</h4>
                    <p style="margin-top: 15px;">
                        <i class="fas fa-map-marker-alt"></i> Jl. Raya Bekasi KM 25, No. 123<br>
                        Bekasi Timur, Jawa Barat 17111<br>
                        <i class="fas fa-phone"></i> (021) 8895-6734<br>
                        <i class="fab fa-whatsapp"></i> 0812-3456-7890
                    </p>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2023 Toko Berkah Abadi. Semua hak dilindungi.</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile Menu Toggle
        document.getElementById('mobileMenu').addEventListener('click', function() {
            document.getElementById('navMenu').classList.toggle('active');
        });
        
        // Form Submission
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const name = document.getElementById('name').value;
            const phone = document.getElementById('phone').value;
            const message = document.getElementById('message').value;
            
            // Create WhatsApp message
            const whatsappMessage = `Halo Toko Berkah Abadi,%0A%0ANama: ${name}%0ANomor HP: ${phone}%0APesan: ${message}`;
            
            // Open WhatsApp
            window.open(`https://wa.me/6281234567890?text=${whatsappMessage}`, '_blank');
            
            // Reset form
            document.getElementById('contactForm').reset();
            
            // Show alert
            alert('Terima kasih! Anda akan diarahkan ke WhatsApp untuk mengirim pesan.');
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if(targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if(targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                    
                    // Close mobile menu if open
                    document.getElementById('navMenu').classList.remove('active');
                }
            });
        });
    </script>
</body>
</html>
```


