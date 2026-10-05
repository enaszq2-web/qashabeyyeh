<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Elegance & Co. | Women's Fashion Boutique Amman</title>
    <style>
        :root {
            --primary: #1a1a1a;
            --accent: #b89753;
            --bg: #faf9f6;
            --card-bg: #ffffff;
            --text: #2c2c2c;
        }
        * { box-sizing: border-box; margin: 0; padding: 0; font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif; }
        body { background-color: var(--bg); color: var(--text); line-height: 1.6; }
        
        header { background: var(--primary); color: #fff; padding: 25px 35px; display: flex; justify-content: space-between; align-items: center; border-bottom: 2px solid var(--accent); position: sticky; top: 0; z-index: 100; }
        .logo { font-size: 1.6rem; font-weight: 700; letter-spacing: 2px; text-transform: uppercase; color: #fff; }
        .logo span { color: var(--accent); }
        .header-tag { font-size: 0.85rem; color: var(--accent); font-weight: 600; text-transform: uppercase; letter-spacing: 1px; }

        .hero { background: linear-gradient(rgba(0,0,0,0.45), rgba(0,0,0,0.45)), url('https://images.unsplash.com/photo-1490481651871-ab68de25d43d?auto=format&fit=crop&w=1600&q=80') center/cover no-repeat; color: #fff; padding: 90px 20px; text-align: center; }
        .hero h1 { font-size: 2.6rem; margin-bottom: 12px; font-weight: 300; letter-spacing: 1px; }
        .hero h1 strong { font-weight: 700; color: var(--accent); }
        .hero p { font-size: 1.05rem; max-width: 600px; margin: 0 auto; color: #e5e5e5; }

        .container { max-width: 1200px; margin: 40px auto; padding: 0 20px; }
        .section-title { text-align: center; margin-bottom: 40px; }
        .section-title h2 { font-size: 2rem; color: var(--primary); margin-bottom: 8px; text-transform: uppercase; letter-spacing: 1px; font-weight: 400; }
        .section-title p { color: #666; font-size: 0.95rem; }

        .products-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 30px; }
        .product-card { background: var(--card-bg); border-radius: 8px; overflow: hidden; box-shadow: 0 5px 15px rgba(0,0,0,0.04); transition: transform 0.3s ease, box-shadow 0.3s ease; display: flex; flex-direction: column; }
        .product-card:hover { transform: translateY(-5px); box-shadow: 0 10px 25px rgba(0,0,0,0.08); }
        
        .product-img { height: 360px; background-size: cover; background-position: center; position: relative; }
        .badge-tag { position: absolute; top: 15px; left: 15px; background: var(--accent); color: #fff; font-size: 0.75rem; font-weight: bold; padding: 5px 10px; border-radius: 4px; text-transform: uppercase; letter-spacing: 1px; }

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
        <div class="logo">Elegance <span>& Co.</span></div>
        <div class="header-tag">Amman Boutique Demo</div>
    </header>

    <div class="hero">
        <h1>Elevate Your <strong>Everyday Style</strong></h1>
        <p>Discover our exclusive Amman collection. Handcrafted elegance delivered straight to your doorstep.</p>
    </div>

    <div class="container">
        <div class="section-title">
            <h2>New Season Arrivals</h2>
            <p>Select your favorite piece, pick your size, and order instantly via WhatsApp.</p>
        </div>

        <div class="products-grid">
            <!-- Product 1 -->
            <div class="product-card">
                <div class="product-img" style="background-image: url('https://images.unsplash.com/photo-1583496661160-fb5886a0aaaa?auto=format&fit=crop&w=800&q=80');">
                    <span class="badge-tag">Bestseller</span>
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
                <div class="product-img" style="background-image: url('https://images.unsplash.com/photo-1515886657613-9f3515b0c78f?auto=format&fit=crop&w=800&q=80');">
                    <span class="badge-tag">New Drop</span>
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
                <div class="product-img" style="background-image: url('https://images.unsplash.com/photo-1539109136881-3be0616acf4b?auto=format&fit=crop&w=800&q=80');">
                    <span class="badge-tag">Limited</span>
                </div>
                <div class="product-info">
                    <div class="product-title">Chic Linen Blazer & Trouser Set</div>
                    <div class="product-desc">Structured yet breathable two-piece set engineered for the modern professional working woman in Amman.</div>
                    <div class="product-price">85.00 JOD</div>
                    <div class="size-selector">
                        <label>Select Size:</label>
                        <div class="sizes">
                            <button class="size-btn active" onclick="selectSize(this, 'S')">S</button>
                            <button class="size-btn" onclick="
