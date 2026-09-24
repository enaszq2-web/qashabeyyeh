<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Qashabeyyeh | Official Store Demo</title>
    <style>
        :root {
            --primary: #111111;
            --accent: #c5a059;
            --bg: #f9f9f9;
            --card-bg: #ffffff;
            --text: #333333;
        }
        * { box-sizing: border-box; margin: 0; padding: 0; font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif; }
        body { background-color: var(--bg); color: var(--text); line-height: 1.6; }
        header { background: var(--primary); color: #fff; padding: 20px; text-align: center; }
        header h1 { font-size: 1.8rem; letter-spacing: 2px; text-transform: uppercase; }
        header p { color: var(--accent); font-size: 0.9rem; margin-top: 5px; }
        
        .container { max-width: 1200px; margin: 30px auto; padding: 0 20px; }
        .hero { background: #222; color: #fff; padding: 40px; border-radius: 8px; text-align: center; margin-bottom: 30px; }
        .hero h2 { font-size: 2rem; margin-bottom: 10px; }
        .hero p { color: #ccc; margin-bottom: 20px; }

        .products-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 25px; }
        .product-card { background: var(--card-bg); border-radius: 8px; overflow: hidden; box-shadow: 0 4px 12px rgba(0,0,0,0.05); transition: transform 0.2s; }
        .product-card:hover { transform: translateY(-5px); }
        .product-img { width: 100%; height: 300px; background-color: #eee; display: flex; align-items: center; justify-content: center; color: #777; font-size: 0.9rem; }
        .product-info { padding: 20px; }
        .product-title { font-size: 1.1rem; font-weight: bold; margin-bottom: 8px; }
        .product-price { color: var(--accent); font-weight: bold; font-size: 1.2rem; margin-bottom: 15px; }
        
        .size-selector { margin-bottom: 15px; }
        .size-selector label { font-size: 0.85rem; display: block; margin-bottom: 5px; color: #666; }
        .sizes { display: flex; gap: 8px; }
        .size-btn { padding: 6px 12px; border: 1px solid #ddd; background: #fff; cursor: pointer; border-radius: 4px; font-size: 0.85rem; }
        .size-btn.active { border-color: var(--primary); background: var(--primary); color: #fff; }

        .buy-btn { display: block; width: 100%; padding: 12px; background: var(--primary); color: #fff; border: none; border-radius: 4px; font-weight: bold; cursor: pointer; text-align: center; text-decoration: none; transition: background 0.2s; }
        .buy-btn:hover { background: var(--accent); }

        footer { text-align: center; padding: 40px; color: #777; font-size: 0.85rem; border-top: 1px solid #eee; margin-top: 50px; }
    </style>
</head>
<body>

    <header>
        <h1>Qashabeyyeh</h1>
        <p>Custom GitHub Storefront Demo - 24/7 Instant Ordering</p>
    </header>

    <div class="container">
        <div class="hero">
            <h2>New Streetwear Collection</h2>
            <p>Browse our latest designs and order instantly via WhatsApp with zero friction.</p>
        </div>

        <div class="products-grid">
            <!-- Product 1 -->
            <div class="product-card">
                <div class="product-img" style="background: #e2e8f0;">Product Image 1</div>
                <div class="product-info">
                    <div class="product-title">Heritage Embroidered Hoodie</div>
                    <div class="product-price">35.00 JOD</div>
                    <div class="size-selector">
                        <label>Select Size:</label>
                        <div class="sizes">
                            <button class="size-btn active" onclick="selectSize(this, 'S')">S</button>
                            <button class="size-btn" onclick="selectSize(this, 'M')">M</button>
                            <button class="size-btn" onclick="selectSize(this, 'L')">L</button>
                            <button class="size-btn" onclick="selectSize(this, 'XL')">XL</button>
                        </div>
                    </div>
                    <a href="#" class="buy-btn" onclick="orderOnWhatsApp('Heritage Embroidered Hoodie', '35.00 JOD', this)">Order via WhatsApp</a>
                </div>
            </div>

            <!-- Product 2 -->
            <div class="product-card">
                <div class="product-img" style="background: #cbd5e1;">Product Image 2</div>
                <div class="product-info">
                    <div class="product-title">Amman Streetwear Oversized Tee</div>
                    <div class="product-price">20.00 JOD</div>
                    <div class="size-selector">
                        <label>Select Size:</label>
                        <div class="sizes">
                            <button class="size-btn active" onclick="selectSize(this, 'S')">S</button>
                            <button class="size-btn" onclick="selectSize(this, 'M')">M</button>
                            <button class="size-btn" onclick="selectSize(this, 'L')">L</button>
                        </div>
                    </div>
                    <a href="#" class="buy-btn" onclick="orderOnWhatsApp('Amman Streetwear Oversized Tee', '20.00 JOD', this)">Order via WhatsApp</a>
                </div>
            </div>
        </div>
    </div>

    <footer>
        <p>&copy; 2026 Qashabeyyeh. Powered by Custom GitHub E-commerce Solution.</p>
    </footer>

    <script>
        function selectSize(button, size) {
            const container = button.parentElement;
            container.querySelectorAll('.size-btn').forEach(btn => btn.classList.remove('active'));
            button.classList.add('active');
        }

        function orderOnWhatsApp(productName, price, element) {
            const card = element.closest('.product-card');
            const selectedSizeBtn = card.querySelector('.size-btn.active');
            const size = selectedSizeBtn ? selectedSizeBtn.innerText : 'Standard';
            
            // استبدل هذا الرقم برقم واتساب التاجر الفعلي
            const phoneNumber = "962790000000"; 
            const message = `Hello, I would like to order:\n- Product: ${productName}\n- Size: ${size}\n- Price: ${price}\n\nPlease confirm availability!`;
            
            const whatsappUrl = `https://wa.me/${phoneNumber}?text=${encodeURIComponent(message)}`;
            window.open(whatsappUrl, '_blank');
        }
    </script>
</body>
</html>
