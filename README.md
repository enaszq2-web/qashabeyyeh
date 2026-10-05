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
        
        /* 1. Live Amman Weather Banner */
        .weather-banner { background: #1c1c1c; color: #f5f5f5; padding: 12px 20px; text-align: center; font-size: 0.9rem; border-bottom: 2px solid var(--accent); display: block; font-weight: 500; }
        .weather-banner span { color: var(--accent); font-weight: 700; }

        header { background: var(--primary); color: #fff; padding: 20px 40px; display: flex; justify-content: space-between; align-items: center; border-bottom: 2px solid var(--accent); position: sticky; top: 0; z-index: 100; }
        
        .brand-container { display: flex; align-items: center; gap: 15px; }
        .logo-mark { width: 45px; height: 45px; background: var(--accent); color: var(--primary); font-weight: 900; font-size: 1.3rem; display: flex; align-items: center; justify-content: center; border-radius: 50%; }
        .logo-text h1 { font-size: 1.4rem; letter-spacing: 2px; text-transform: uppercase; color: #fff; line-height: 1.1; }
        .logo-text p { font-size: 0.75rem; color: var(--accent); letter-spacing: 1.5px; text-transform: uppercase; }

        .header-badge { background: rgba(197, 160, 89, 0.15); color: var(--accent); border: 1px solid var(--accent); padding: 6px 14px; border-radius: 20px; font-size: 0.75rem; font-weight: bold; text-transform: uppercase; letter-spacing: 1px; }

        .hero { background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1490481651871-ab68de25d43d?auto=format&fit=crop&w=1600&q=80') center/cover no-repeat; color: #fff; padding: 75px 20px; text-align: center; }
        .hero h2 { font-size: 2.5rem; margin-bottom: 12px; font-weight: 300; letter-spacing: 1px; }
        .hero h2 strong { font-weight: 700; color: var(--accent); }
        .hero p { font-size: 1.05rem; max-width: 650px; margin: 0 auto; color: #e5e5e5; }

        .container { max-width: 1200px; margin: 40px auto; padding: 0 20px; }
        
        /* 2. AI Interactive Fit Recommender Module (Height/Weight Inputs) */
        .ai-fit-box { background: #fff; border: 2px solid var(--accent); border-radius: 10px; padding: 30px; margin-bottom: 45px; box-shadow: 0 6px 20px rgba(0,0,0,0.06); }
        .ai-fit-header { margin-bottom: 20px; }
        .ai-fit-header h3 { font-size: 1.2rem; color: var(--primary); display: flex; align-items: center; gap: 10px; }
        .ai-fit-header h3 span { background: var(--accent); color: #fff; font-size: 0.7rem; padding: 4px 10px; border-radius: 4px; text-transform: uppercase; font-weight: bold; }
        .ai-fit-header p { font-size: 0.9rem; color: #666; margin-top: 5px; }
        
        .ai-inputs-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)) 160px; gap: 20px; align-items: flex-end; }
        .ai-field { display: flex; flex-direction: column; gap: 8px; }
        .ai-field label { font-size: 0.8rem; font-weight: 700; text-transform: uppercase; color: #333; letter-spacing: 0.5px; }
        .ai-input, .ai-select { padding: 12px 16px; border: 1px solid #bbb; border-radius: 6px; font-size: 0.95rem; outline: none; background: #fff; width: 100%; color: #111; }
        .ai-input:focus, .ai-select:focus { border-color: var(--accent); box-shadow: 0 0 5px rgba(197, 160, 89, 0.3); }
        
        .ai-btn { padding: 12px 20px; background: var(--primary); color: var(--accent); border: none; border-radius: 6px; font-weight: bold; cursor: pointer; text-transform: uppercase; font-size: 0.85rem; letter-spacing: 1px; transition: all 0.2s; height: 46px; width: 100%; }
        .ai-btn:hover { background: var(--accent); color: var(--primary); }
        
        #aiResultMsg { width: 100%; font-size: 0.95rem; color: #155724; font-weight: 600; margin-top: 20px; background: #d4edda; border: 1px solid #c3e6cb; padding: 14px 18px; border-radius: 6px; display: none; }

        .section-title { text-align: center; margin-bottom: 40px; }
        .section-title h2 { font-size: 2rem; color: var(--primary); margin-bottom: 8px; text-transform: uppercase; letter-spacing: 1px; font-weight: 400; }
        .section-title p { color: #666; font-size: 0.95rem; }

        .products-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 30px; }
        .product-card { background: var(--card-bg); border-radius: 10px; overflow: hidden; box-shadow: 0 6px 20px rgba(0,0,0,0.06); transition: transform 0.3s ease; display: flex; flex-direction: column; border: 1px solid #eee; }
        .product-card:hover { transform: translateY(-5px); }
        
        /* 3. Multi-angle Image Slider styling */
        .product-img-slider { height: 380px; position: relative; background: #111; overflow: hidden; }
        .slide-img { width: 100%; height: 100%; object-fit: cover; position: absolute; top: 0; left: 0; opacity: 0; transition: opacity 0.5s ease-in-out; }
        .slide-img.active { opacity: 1; position: relative; }
        
        .badge-tag { position: absolute; top: 15px; left: 15px; background: var(--accent); color: #fff; font-size: 0.75rem; font-weight: bold; padding: 6px 12px; border-radius: 4px; text-transform: uppercase; letter-spacing: 1px; z-index: 20;
