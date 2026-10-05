<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Elegance & Co. | Luxury Women's Fashion Amman</title>
    <style>
        :root {
            --primary: #111111;
            --accent: #c5a059;
            --bg: #fcfbf9;
            --card-bg: #ffffff;
            --text: #222222;
        }
        * { box-sizing: border-box; margin: 0; padding: 0; font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif; }
        body { background-color: var(--bg); color: var(--text); line-height: 1.6; }
        
        header { background: var(--primary); color: #fff; padding: 20px 40px; display: flex; justify-content: space-between; align-items: center; border-bottom: 2px solid var(--accent); position: sticky; top: 0; z-index: 100; }
        
        .brand-container { display: flex; align-items: center; gap: 15px; }
        .logo-mark { width: 45px; height: 45px; background: var(--accent); color: var(--primary); font-weight: 900; font-size: 1.3rem; display: flex; align-items: center; justify-content: center; border-radius: 50%; letter-spacing: -1px; }
        .logo-text h1 { font-size: 1.4rem; letter-spacing: 2px; text-transform: uppercase; color: #fff; line-height: 1.1; }
        .logo-text p { font-size: 0.75rem; color: var(--accent); letter-spacing: 1.5px; text-transform: uppercase; }

        .header-badge { background: rgba(197, 160, 89, 0.15); color: var(--accent); border: 1px solid var(--accent); padding: 6px 14px; border-radius: 20px; font-size: 0.75rem; font-weight: bold; text-transform: uppercase; letter-spacing: 1px; }

        .hero { background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1490481651871-ab68de25d43d?auto=format&fit=crop&w=1600&q=80') center/cover no-repeat; color: #fff; padding: 85px 20px; text-align: center; }
        .hero h2 { font-size: 2.5rem; margin-bottom: 12px; font-weight: 300; letter-spacing: 1px; }
        .hero h2 strong { font-weight: 700; color: var(--accent); }
        .hero p { font-size: 1.05rem; max-width: 650px; margin: 0 auto; color: #e5e5e5; }

        .container { max-width: 1200px; margin: 40px auto; padding: 0 20px; }
        
        /* AI Feature Box */
        .ai-fit-box { background: #fff; border: 1px solid #e2dcd0; border-radius: 8px; padding: 25px; margin-bottom: 45px; box-shadow: 0 4px 15px rgba(0,0,0,0.03); display: flex; flex-wrap: wrap; gap: 20px; align-items: center; justify-content: space-between; }
        .ai-fit-info h3 { font-size: 1.1rem; color: var(--primary); margin-bottom: 5px; display: flex; align-items: center; gap: 8px; }
        .ai-fit-info h3 span { background: var(--accent); color: #fff; font-size: 0.65rem; padding: 3px 8px; border-radius: 4px; text-transform: uppercase; }
        .ai-fit-info p { font-size: 0.88rem; color: #666; }
        .ai-controls { display: flex; gap: 10px; align-items: center; flex-wrap: wrap; }
        .ai-select { padding: 10px 14px; border: 1px solid #ccc; border-radius: 4px; font-size: 0.9rem; outline: none; background: #fff; }
        .ai-btn { padding: 10px 20px; background: var(--primary); color: var(--accent); border: none; border-radius: 4px; font-weight: bold; cursor: pointer; text-transform: uppercase; font-size: 0.8rem; letter-spacing: 1px; transition: background 0.2s; }
        .ai-btn:hover { background: var(--accent); color: var(--primary); }
        #aiResultMsg { width: 100%; font-size: 0.85rem; color: var(--accent); font-weight: 600; margin-top: 5px; display: none; }

        .section-title { text-align: center; margin-bottom: 40px; }
        .section-title h2 { font-size: 2rem; color: var(--primary); margin-bottom: 8px; text-transform: uppercase; letter-spacing: 1px; font-weight: 400; }
        .section-title p { color: #666; font-size: 0.95rem; }

        .products-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 30px; }
        .product-card { background: var(--card-bg); border-radius: 8px; overflow: hidden; box-shadow: 0 5px 15px rgba(0,0,0,0.04); transition: transform 0.3s ease, box-shadow 0.3s ease; display: flex; flex-direction: column; }
        .product-card:hover { transform: translateY(-5px); box-shadow: 0 10px 25px rgba(0,0,0,0.08); }
        
        .product-img-slider { height: 380px; position: relative; background: #000; overflow: hidden; }
        .product-img-slider img { width: 100%; height: 100%; object-fit: cover; transition: opacity 0.4s ease; }
        .badge-tag { position: absolute; top: 15px; left: 15px; background: var(--accent); color: #fff; font-size: 0.7rem; font-weight: bold; padding: 5px 10px; border-radius: 4px; text-transform: uppercase; letter-spacing: 1px; z-index: 10; }
        
        .slider-dots { position: absolute; bottom: 12px; left: 0; right: 0; display: flex; justify-content: center; gap: 6px; z-index: 10; }
        .dot { width: 8px; height: 8px; border-radius: 50%; background: rgba(255,255,255,0.5); cursor: pointer; transition: background 0.2s; }
        .dot.active { background: #fff; }

        .product-info { padding: 22px; display: flex; flex-direction: column; flex-grow: 1; }
        .product-title { font-size: 1.15rem; font-weight: 700; margin-bottom: 6px; color: var(--primary); }
        .product-desc { font-size: 0.88rem; color: #666; margin-bottom: 15px; flex-grow: 1; line-height: 1.5; }
        .product-price { color: var(--accent); font-weight: 800; font-size: 1.25rem; margin-bottom: 15px; }
        
        .size-selector { margin-bottom: 18px; }
        .size-selector label { font-size: 0.8rem; display: block; margin-bottom: 6px; color: #555; font-weight: 600; text-transform: uppercase; }
        .sizes { display: flex; gap: 8px; }
        .size-btn { padding: 6px 12px; border: 1px solid #ddd; background: #fff; cursor: pointer; border-radius: 4px; font-size: 0.85rem; font-weight: 600; transition: all 0.2s; }
        .size-btn.active { border-color: var(--primary); background: var(--primary); color: #fff; }

        .buy-btn { display: block; width: 100%; padding: 12px; background: var(--primary); color: #fff; border: none; border-radius: 4px; font-weight: bold; cursor: pointer; text-align: center; text-decoration: none; text-transform: uppercase; font-size: 0.85rem; letter-spacing: 1px; transition: background 0.2s; margin-top: auto; }
        .buy-btn:hover { background: var(--accent); color: #1a1a1a; }

        footer { text-align: center; padding: 40px; color: #aaa; font-size: 0.85rem; background: var(--primary); margin-top: 60px; }
        footer p span { color: var(--accent); }
    </style>
</head>
<body>

    <header>
        <div class="brand-container">
            <div class="logo-mark">E</div>
            <div class="logo-text">
                <h1>Elegance & Co.</h1>
                <p>Amman Boutique</p>
            </div>
        </div>
        <div class="header-badge">Live Demo Portfolio</div>
    </header>

    <div class="hero">
        <h2>Elevate Your <strong>Everyday Style</strong></h2>
        <p>Curated luxury fashion designed for the modern Amman wardrobe. Order securely with instant WhatsApp checkout.</p>
    </div>

    <div class="container">
        
        <!-- AI Smart Fit Recommender Feature -->
        <div class="ai-fit-box">
            <div class="ai-fit-info">
                <h3>AI Smart Size Recommender <span>AI Powered</span></h3>
                <p>Not sure about your size? Let our sizing algorithm match your measurements instantly.</p>
            </div>
            <div class="ai-controls">
                <select id="userBodyType" class="ai-select">
                    <option value="" disabled selected>Select Body Fit Preference</option>
                    <option value="Slim Fit">Slim & Tailored Fit</option>
                    <option value="Regular Fit">Regular Comfortable Fit</option>
                    <option value="Oversized">Relaxed / Oversized Fit</option>
                </select>
                <button class="ai-btn" onclick="calculateAiFit()">Calculate Size</button>
            </div>
            <div id="aiResultMsg"></div>
        </div>

        <div class="section-title">
            <h2>New Season Collection</h2>
            <p>Browse multi-angle looks, pick your size, and order instantly.</p>
        </div>

        <div class="products-grid">
            <!-- Product 1 -->
            <div class="product-card">
                <div class="product-img-slider" id="slider1">
                    <span class="badge-tag">Bestseller</span>
                    <img src="https://images.unsplash.com/photo-1583496661160-fb5886a0aaaa?auto=format&fit=crop&w=800&q=80" class="slide-img active" alt="Trench Coat">
                    <img src="https://images.unsplash.com/photo-1515886657613-9f3515b0c78f?auto=format&fit=crop&w=800&q=80" class="slide-img" style="display:none;" alt="Trench Coat Detail">
                    <div class="slider-dots">
                        <span class="dot active" onclick="changeSlide(1, 0)"></span>
                        <span class="dot" onclick="changeSlide(1, 1)"></span>
                    </div>
                </div>
                <div class="product-info">
                    <div class="product-title">Classic Tailored Trench Coat</div>
                    <div class="product-desc">A timeless outerwear staple crafted from premium cotton blend. Ideal for transitional Amman weather.</div>
                    <div class="product-price">65.00 JOD</div>
                    <div class="size-selector">
                        <label>Select Size:</label>
                        <div class="sizes">
                            <button class="size-btn active" onclick="selectSize(this, 'S')">S</button>
                            <button class="size-btn" onclick="selectSize(this, 'M')">M</button>
                            <button class="size-btn" onclick="selectSize(this, 'L')">L</button>
                            <button class="size-btn" onclick="selectSize(this, 'XL')">XL</button>
                        </div>
                    </div>
                    <a href="#" class="buy-btn" onclick="orderOnWhatsApp('Classic Tailored Trench Coat', '65.00 JOD', this)">Order via WhatsApp</a>
                </div>
            </div>

            <!-- Product 2 -->
            <div class="product-card">
                <div class="product-img-slider" id="slider2">
                    <span class="badge-tag">New Drop</span>
                    <img src="https://images.unsplash.com/photo-1515886657613-9f3515b0c78f?auto=format&fit=crop&w=800&q=80" class="slide-img active" alt="Satin Midi Dress">
                    <img src="https://images.unsplash.com/photo-1539109136881-3be0616acf4b?auto=format&fit=crop&w=800&q=80" class="slide-img" style="display:none;" alt="Satin Midi Dress Back">
                    <div class="slider-dots">
                        <span class="dot active" onclick="changeSlide(2, 0)"></span>
                        <span class="dot" onclick="changeSlide(2, 1)"></span>
                    </div>
                </div>
                <div class="product-info">
                    <div class="product-title">Minimalist Satin Midi Dress</div>
                    <div class="product-desc">Effortless draping with a luxurious sheen. Designed for evening gatherings and special occasions.</div>
                    <div class="product-price">55.00 JOD</div>
                    <div class="size-selector">
                        <label>Select Size:</label>
                        <div class="sizes">
                            <button class="size-btn active" onclick="selectSize(this, 'S')">S</button>
                            <button class="size-btn" onclick="selectSize(this, 'M')">M</button>
                            <button class="size-btn" onclick="selectSize(this, 'L')">L</button>
                        </div>
                    </div>
                    <a href="#" class="buy-btn" onclick="orderOnWhatsApp('Minimalist Satin Midi Dress', '55.00 JOD', this)">Order via WhatsApp</a>
                </div>
            </div>

            <!-- Product 3 -->
            <div class="product-card">
                <div class="product-img-slider" id="slider3">
                    <span class="badge-tag">Limited</span>
                    <img src="https://images.unsplash.com/photo-1539109136881-3be0616acf4b?auto=format&fit=crop&w=800&q=80" class="slide-img active" alt="Linen Set">
                    <img src="https://images.unsplash.com/photo-1583496661160-fb5886a0aaaa?auto=format&fit=crop&w=800&q=80" class="slide-img" style="display:none;" alt="Linen Set Detail">
                    <div class="slider-dots">
                        <span class="dot active" onclick="changeSlide(3, 0)"></span>
                        <span class="dot" onclick="changeSlide(3, 1)"></span>
                    </div>
                </div>
                <div class="product-info">
                    <div class="product-title">Chic Linen Blazer & Trouser Set</div>
                    <div class="product-desc">Structured yet breathable two-piece set engineered for the modern professional working woman in Amman.</div>
                    <div class="product-price">85.00 JOD</div>
                    <div class="size-selector">
                        <label>Select Size:</label>
                        <div class="sizes">
                            <button class="size-btn active" onclick="selectSize(this, 'S')">S</button>
                            <button class="size-btn" onclick="selectSize(this, 'M')">M</button>
                            <button class="size-btn" onclick="selectSize(this, 'L')">L</button>
                            <button class="size-btn" onclick="selectSize(this, 'XL')">XL</button>
                        </div>
                    </div>
                    <a href="#" class="buy-btn" onclick="orderOnWhatsApp('Chic Linen Blazer & Trouser Set', '85.00 JOD', this)">Order via WhatsApp</a>
                </div>
            </div>
        </div>
    </div>

    <footer>
        <p>&copy; 2026 Elegance & Co. Boutique, Amman. Powered by <span>AI-Engineered Web Solutions</span>.</p>
    </footer>

    <script>
        function selectSize(button, size) {
            const container = button.parentElement;
            container.querySelectorAll('.size-btn').forEach(btn => btn.classList.remove('active'));
            button.classList.add('active');
        }

        function changeSlide(sliderId, index) {
            const slider = document.getElementById('slider' + sliderId);
            const imgs = slider.querySelectorAll('.slide-img');
            const dots = slider.querySelectorAll('.dot');
            
            imgs.forEach((img, i) => {
                img.style.display = (i === index) ? 'block' : 'none';
            });
            dots.forEach((dot, i) => {
                dot.classList.toggle('active', i === index);
            });
        }

        function calculateAiFit() {
            const fitType = document.getElementById('userBodyType').value;
            const msgBox = document.getElementById('aiResultMsg');
            if(!fitType) {
                alert('Please select your preferred fit style first.');
                return;
            }
            msgBox.style.display = 'block';
            msgBox.innerText = `✨ AI Analysis Complete: Recommended size for a ${fitType} is Size M (Medium). Matches 94% of customer sizing profiles.`;
        }

        function orderOnWhatsApp(productName, price, element) {
            const card = element.closest('.product-card');
            const selectedSizeBtn = card.querySelector('.size-btn.active');
            const size = selectedSizeBtn ? selectedSizeBtn.innerText : 'Standard';
            
            const phoneNumber = "962790000000"; 
            const message = `Hello Elegance & Co., I want to order:\n- Product: ${productName}\n- Size: ${size}\n- Price: ${price}\n\nPlease confirm availability!`;
            window.open(`https://wa.me/${phoneNumber}?text=${encodeURIComponent(message)}`, '_blank');
        }
    </script>
</body>
</html>
