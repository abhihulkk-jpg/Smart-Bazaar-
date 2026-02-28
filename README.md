# Smart-Bazaar-<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SmartBazar \u2013 Best Quality Delivered</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;900&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --ink: #1a1a2e;
    --cream: #fdf8f3;
    --saffron: #e8621a;
    --saffron-light: #ff7a32;
    --gold: #f4c430;
    --muted: #7a7a8c;
    --card-bg: #ffffff;
    --border: #ece6df;
    --success: #2d8c4e;
    --radius: 16px;
    --shadow: 0 4px 24px rgba(26,26,46,0.10);
    --shadow-hover: 0 12px 40px rgba(232,98,26,0.18);
  }
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; }
  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--cream);
    color: var(--ink);
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* \u2500\u2500 HEADER \u2500\u2500 */
  header {
    background: var(--ink);
    color: var(--cream);
    padding: 0 20px;
    position: sticky; top: 0; z-index: 100;
    display: flex; align-items: center; justify-content: space-between;
    height: 64px;
    box-shadow: 0 2px 16px rgba(0,0,0,0.18);
  }
  .brand { display: flex; flex-direction: column; line-height: 1.1; }
  .brand-name {
    font-family: 'Playfair Display', serif;
    font-size: 1.45rem; font-weight: 900;
    color: var(--gold);
    letter-spacing: -0.5px;
  }
  .brand-tag { font-size: 0.68rem; color: #b0afc0; font-weight: 300; letter-spacing: 0.3px; }
  .header-right { display: flex; align-items: center; gap: 12px; }
  .cart-btn {
    background: var(--saffron);
    border: none; color: #fff;
    border-radius: 50px; padding: 8px 16px 8px 12px;
    font-family: 'DM Sans', sans-serif; font-size: 0.9rem; font-weight: 600;
    cursor: pointer; display: flex; align-items: center; gap: 6px;
    transition: background 0.2s, transform 0.15s;
    position: relative;
  }
  .cart-btn:hover { background: var(--saffron-light); transform: scale(1.04); }
  .cart-count {
    background: var(--gold); color: var(--ink);
    border-radius: 50%; width: 20px; height: 20px;
    font-size: 0.72rem; font-weight: 700;
    display: flex; align-items: center; justify-content: center;
    transition: transform 0.2s;
  }
  .cart-count.bump { animation: bump 0.3s ease; }
  @keyframes bump { 0%,100%{transform:scale(1)} 50%{transform:scale(1.4)} }

  /* \u2500\u2500 HERO \u2500\u2500 */
  .hero {
    position: relative; height: 320px; overflow: hidden;
    display: flex; align-items: flex-end;
  }
  .hero img {
    position: absolute; inset: 0; width: 100%; height: 100%;
    object-fit: cover; object-position: center top;
    filter: brightness(0.55);
  }
  .hero-content {
    position: relative; z-index: 2;
    padding: 28px 24px;
    background: linear-gradient(to top, rgba(26,26,46,0.85) 0%, transparent 100%);
    width: 100%;
  }
  .hero-content h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.6rem, 5vw, 2.6rem);
    color: #fff; line-height: 1.15; font-weight: 900;
    text-shadow: 0 2px 12px rgba(0,0,0,0.4);
  }
  .hero-content h1 span { color: var(--gold); }
  .hero-content p {
    color: #ddd; margin-top: 6px; font-size: 0.9rem; font-weight: 300;
  }
  .hero-content p strong { color: var(--gold); }

  /* \u2500\u2500 FILTERS \u2500\u2500 */
  .filters-wrap { padding: 20px 16px 8px; }
  .filters-label { font-size: 0.72rem; color: var(--muted); font-weight: 500; letter-spacing: 1px; text-transform: uppercase; margin-bottom: 10px; }
  .filters { display: flex; gap: 8px; flex-wrap: wrap; }
  .filter-btn {
    background: var(--card-bg); border: 1.5px solid var(--border);
    border-radius: 50px; padding: 7px 18px; font-size: 0.85rem;
    font-family: 'DM Sans', sans-serif; font-weight: 500; color: var(--ink);
    cursor: pointer; transition: all 0.18s;
  }
  .filter-btn:hover { border-color: var(--saffron); color: var(--saffron); }
  .filter-btn.active { background: var(--saffron); border-color: var(--saffron); color: #fff; }

  /* \u2500\u2500 PRODUCTS \u2500\u2500 */
  .section-title {
    padding: 8px 20px 4px;
    font-family: 'Playfair Display', serif;
    font-size: 1.25rem; font-weight: 700; color: var(--ink);
  }
  .products-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(155px, 1fr));
    gap: 14px; padding: 12px 16px 100px;
  }
  .product-card {
    background: var(--card-bg);
    border-radius: var(--radius);
    box-shadow: var(--shadow);
    overflow: hidden;
    display: flex; flex-direction: column;
    transition: box-shadow 0.22s, transform 0.22s;
    border: 1px solid var(--border);
  }
  .product-card:hover { box-shadow: var(--shadow-hover); transform: translateY(-4px); }
  .product-img-wrap {
    width: 100%; aspect-ratio: 1/1; overflow: hidden; background: #f5f0ea;
  }
  .product-img-wrap img {
    width: 100%; height: 100%; object-fit: cover;
    transition: transform 0.35s ease;
  }
  .product-card:hover .product-img-wrap img { transform: scale(1.07); }
  .product-info { padding: 10px 12px 12px; display: flex; flex-direction: column; gap: 4px; flex: 1; }
  .product-cat {
    font-size: 0.65rem; text-transform: uppercase; letter-spacing: 1px;
    color: var(--saffron); font-weight: 600;
  }
  .product-name { font-size: 0.88rem; font-weight: 600; color: var(--ink); line-height: 1.3; }
  .product-desc { font-size: 0.75rem; color: var(--muted); line-height: 1.4; }
  .product-footer { display: flex; align-items: center; justify-content: space-between; margin-top: 8px; }
  .product-price { font-size: 1rem; font-weight: 700; color: var(--saffron); }
  .add-btn {
    background: var(--ink); color: #fff;
    border: none; border-radius: 8px; padding: 6px 12px;
    font-size: 0.78rem; font-weight: 600; cursor: pointer;
    font-family: 'DM Sans', sans-serif;
    transition: background 0.18s, transform 0.15s;
    white-space: nowrap;
  }
  .add-btn:hover { background: var(--saffron); transform: scale(1.05); }
  .add-btn.added { background: var(--success); }

  /* \u2500\u2500 WHATSAPP FLOAT \u2500\u2500 */
  .wa-float {
    position: fixed; bottom: 80px; right: 16px; z-index: 99;
    background: #25d366; color: #fff;
    border-radius: 50%; width: 52px; height: 52px;
    display: flex; align-items: center; justify-content: center;
    box-shadow: 0 4px 20px rgba(37,211,102,0.4);
    text-decoration: none; font-size: 1.5rem;
    transition: transform 0.2s, box-shadow 0.2s;
    animation: float 3s ease-in-out infinite;
  }
  .wa-float:hover { transform: scale(1.12); box-shadow: 0 8px 28px rgba(37,211,102,0.55); animation: none; }
  @keyframes float { 0%,100%{transform:translateY(0)} 50%{transform:translateY(-6px)} }

  /* \u2500\u2500 CART OVERLAY \u2500\u2500 */
  .overlay {
    position: fixed; inset: 0; background: rgba(26,26,46,0.5);
    z-index: 200; opacity: 0; pointer-events: none;
    transition: opacity 0.25s;
    backdrop-filter: blur(2px);
  }
  .overlay.open { opacity: 1; pointer-events: all; }

  .cart-panel {
    position: fixed; top: 0; right: 0; bottom: 0;
    width: min(420px, 100vw);
    background: var(--cream); z-index: 201;
    display: flex; flex-direction: column;
    transform: translateX(100%); transition: transform 0.3s cubic-bezier(.4,0,.2,1);
    box-shadow: -8px 0 40px rgba(0,0,0,0.14);
  }
  .cart-panel.open { transform: translateX(0); }

  .cart-header {
    background: var(--ink); color: #fff;
    padding: 18px 20px; display: flex; align-items: center; justify-content: space-between;
  }
  .cart-header h2 { font-family: 'Playfair Display', serif; font-size: 1.2rem; font-weight: 700; }
  .close-btn {
    background: rgba(255,255,255,0.12); border: none; color: #fff;
    border-radius: 50%; width: 34px; height: 34px;
    font-size: 1.1rem; cursor: pointer; display: flex; align-items: center; justify-content: center;
    transition: background 0.18s;
  }
  .close-btn:hover { background: rgba(255,255,255,0.25); }

  .cart-items { flex: 1; overflow-y: auto; padding: 16px; display: flex; flex-direction: column; gap: 10px; }
  .empty-cart { text-align: center; padding: 48px 20px; color: var(--muted); }
  .empty-cart .icon { font-size: 3rem; margin-bottom: 12px; }
  .empty-cart p { font-size: 0.95rem; }

  .cart-item {
    background: var(--card-bg); border-radius: 12px; border: 1px solid var(--border);
    padding: 12px; display: flex; gap: 10px; align-items: center;
    animation: slideIn 0.25s ease;
  }
  @keyframes slideIn { from{opacity:0;transform:translateX(30px)} to{opacity:1;transform:none} }
  .cart-item-img { width: 56px; height: 56px; border-radius: 8px; object-fit: cover; flex-shrink: 0; }
  .cart-item-info { flex: 1; min-width: 0; }
  .cart-item-name { font-size: 0.85rem; font-weight: 600; white-space: nowrap; overflow: hidden; text-overflow: ellipsis; }
  .cart-item-subtotal { font-size: 0.82rem; color: var(--saffron); font-weight: 700; margin-top: 2px; }
  .cart-item-controls { display: flex; align-items: center; gap: 6px; margin-top: 6px; }
  .qty-btn {
    background: var(--ink); color: #fff;
    border: none; border-radius: 6px; width: 26px; height: 26px;
    font-size: 1rem; cursor: pointer; display: flex; align-items: center; justify-content: center;
    transition: background 0.15s;
  }
  .qty-btn:hover { background: var(--saffron); }
  .qty-display { font-size: 0.9rem; font-weight: 700; min-width: 20px; text-align: center; }
  .remove-btn {
    background: none; border: none; color: #c0392b; font-size: 1rem;
    cursor: pointer; padding: 2px 4px; margin-left: auto;
    transition: transform 0.15s;
  }
  .remove-btn:hover { transform: scale(1.2); }

  .cart-footer { padding: 16px; border-top: 1.5px solid var(--border); background: var(--card-bg); }
  .grand-total-row {
    display: flex; justify-content: space-between; align-items: center;
    font-size: 1.05rem; font-weight: 700; margin-bottom: 14px;
  }
  .grand-total-amount { color: var(--saffron); font-size: 1.2rem; }
  .checkout-btn {
    width: 100%; background: var(--saffron); color: #fff;
    border: none; border-radius: 12px; padding: 14px;
    font-size: 1rem; font-weight: 700; cursor: pointer;
    font-family: 'DM Sans', sans-serif;
    transition: background 0.2s, transform 0.15s;
    letter-spacing: 0.3px;
  }
  .checkout-btn:hover { background: var(--saffron-light); transform: scale(1.02); }
  .checkout-btn:disabled { background: #ccc; cursor: not-allowed; transform: none; }

  /* \u2500\u2500 ORDER MODAL \u2500\u2500 */
  .modal-overlay {
    position: fixed; inset: 0; background: rgba(26,26,46,0.6);
    z-index: 300; display: flex; align-items: flex-end; justify-content: center;
    opacity: 0; pointer-events: none; transition: opacity 0.25s;
    backdrop-filter: blur(3px);
  }
  .modal-overlay.open { opacity: 1; pointer-events: all; }
  .modal {
    background: var(--cream); border-radius: 24px 24px 0 0;
    width: min(480px, 100vw); max-height: 90vh;
    overflow-y: auto; padding: 24px 20px 32px;
    transform: translateY(100%); transition: transform 0.3s cubic-bezier(.4,0,.2,1);
  }
  .modal-overlay.open .modal { transform: translateY(0); }
  .modal h2 {
    font-family: 'Playfair Display', serif; font-size: 1.3rem;
    margin-bottom: 4px;
  }
  .modal-subtitle { color: var(--muted); font-size: 0.82rem; margin-bottom: 20px; }
  .order-summary-box {
    background: var(--card-bg); border: 1px solid var(--border);
    border-radius: 12px; padding: 14px; margin-bottom: 20px; font-size: 0.82rem;
  }
  .order-summary-box h3 { font-size: 0.78rem; text-transform: uppercase; letter-spacing: 1px; color: var(--muted); margin-bottom: 10px; }
  .summary-line { display: flex; justify-content: space-between; padding: 4px 0; border-bottom: 1px dashed var(--border); }
  .summary-line:last-child { border-bottom: none; font-weight: 700; color: var(--saffron); font-size: 0.9rem; }
  .form-group { margin-bottom: 14px; }
  .form-group label { display: block; font-size: 0.8rem; font-weight: 600; margin-bottom: 5px; color: var(--ink); }
  .form-group label span { color: var(--saffron); }
  .form-group input, .form-group textarea {
    width: 100%; border: 1.5px solid var(--border); border-radius: 10px;
    padding: 11px 14px; font-size: 0.9rem; font-family: 'DM Sans', sans-serif;
    background: var(--card-bg); color: var(--ink);
    transition: border-color 0.18s;
    outline: none;
  }
  .form-group input:focus, .form-group textarea:focus { border-color: var(--saffron); }
  .form-group textarea { resize: vertical; min-height: 72px; }
  .submit-order-btn {
    width: 100%; background: var(--saffron); color: #fff;
    border: none; border-radius: 12px; padding: 14px;
    font-size: 1rem; font-weight: 700; cursor: pointer;
    font-family: 'DM Sans', sans-serif; margin-top: 6px;
    transition: background 0.2s, transform 0.15s;
  }
  .submit-order-btn:hover { background: var(--saffron-light); transform: scale(1.02); }
  .modal-close {
    position: absolute; top: 16px; right: 16px;
    background: var(--border); border: none; border-radius: 50%;
    width: 32px; height: 32px; font-size: 1rem; cursor: pointer;
    display: flex; align-items: center; justify-content: center;
    transition: background 0.18s;
  }
  .modal-close:hover { background: #d
