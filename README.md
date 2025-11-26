# Elzawhips
<!doctype html>
<html lang="id">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Elza's Whip — Dessert & Ice Cream</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
<style>
  :root{
    --coksu:#d7b89c;
    --cream:#fff7ee;
    --pink:#f6d7db;
    --accent:#8b5e3c;
    --card:#fffaf6;
    --shadow: 0 8px 30px rgba(0,0,0,0.08);
  }
  *{box-sizing:border-box}
  body{
    margin:0;
    font-family: 'Poppins', sans-serif;
    background: linear-gradient(135deg, #ffeae3, #f5e6dd 40%, #fff5ec 70%);
    color: #5a3e36;
    -webkit-font-smoothing:antialiased;
    min-height:100vh;
    padding:28px 18px;
  }

  header{
    text-align:center;
    padding:18px;
    border-radius:14px;
    background: linear-gradient(90deg, rgba(215,184,156,0.95), rgba(248,214,221,0.95));
    box-shadow: var(--shadow);
    margin-bottom:18px;
  }
  header h1{ margin:6px 0 4px; font-family:'Pacifico', cursive; font-size:2.6rem; color:var(--accent); }
  header p{ margin:2px 0; color:#6b4a3a; }
  header .address{ font-size:13px; color:#6b4a3a; margin-top:4px; }

  main{ max-width:1100px; margin:18px auto; }

  .hero{
    display:flex; gap:18px; align-items:center; justify-content:space-between;
    background: linear-gradient(180deg, rgba(255,255,255,0.7), rgba(255,250,245,0.7));
    padding:16px; border-radius:14px; box-shadow: var(--shadow); margin-bottom:18px;
  }
  .hero .left h2{ margin:0; color:var(--accent); font-size:1.25rem; }
  .hero .left p{ margin:6px 0 0; color:#6b4a3a; }

  .grid{
    display:grid;
    grid-template-columns: repeat(auto-fill, minmax(240px,1fr));
    gap:18px;
    margin-bottom:18px;
  }

  .card{
    background: var(--card);
    border-radius:14px;
    overflow:hidden;
    box-shadow: 0 6px 20px rgba(0,0,0,0.06);
    border:1px solid rgba(139,94,60,0.06);
    transition: transform .18s;
  }
  .card:hover{ transform: translateY(-6px); }
  .imgwrap{ display:block; height:180px; overflow:hidden; }
  .imgwrap img{ width:100%; height:100%; object-fit:cover; display:block; transition: transform .35s; }
  .card:hover .imgwrap img{ transform: scale(1.05); }
  .card-body{ padding:12px; text-align:center; }
  .title{ font-weight:600; color:var(--accent); margin:8px 0 6px; font-size:1.05rem; }
  .desc{ font-size:13px; color:#6b4a3a; min-height:36px; margin:0 0 8px; }
  .price{ font-weight:700; color:#8b4f2a; margin-bottom:10px; }

  .actions{ display:flex; gap:8px; justify-content:center; }
  .btn{
    padding:8px 12px; border-radius:10px; border:none; cursor:pointer; font-weight:600;
    background: linear-gradient(180deg,var(--pink), #ffb6c1); color:white; box-shadow:0 8px 18px rgba(246,215,219,0.35);
  }
  .btn.secondary{ background:transparent; color:var(--accent); border:1px solid rgba(139,94,60,0.12); box-shadow:none; }

  .cart-bar{
    position:fixed; right:18px; bottom:18px; width:320px; max-width:92%;
    background:linear-gradient(180deg,#fff,#fffbf8); border-radius:14px; box-shadow: 0 18px 50px rgba(0,0,0,0.18);
    padding:12px; border:1px solid rgba(139,94,60,0.06);
  }
  .cart-title{ font-weight:700; color:var(--accent); margin:0 0 8px; display:flex; justify-content:space-between; align-items:center;}
  .cart-list{ max-height:240px; overflow:auto; margin-bottom:8px; padding-right:6px; }
  .cart-item{ display:flex; gap:8px; align-items:center; padding:6px 0; border-bottom:1px dashed rgba(139,94,60,0.05); }
  .cart-item img{ width:48px; height:40px; object-fit:cover; border-radius:8px; }
  .cart-item .meta{ font-size:13px; color:#6b4a3a; flex:1; text-align:left; }
  .cart-item .meta .n{ font-weight:600; color:var(--accent); }
  .cart-item .qty{ color:#8b4f2a; font-weight:700; min-width:28px; text-align:right; }

  .cart-footer{ display:flex; justify-content:space-between; align-items:center; gap:8px; }
  .checkout{ padding:8px 10px; border-radius:10px; background:var(--coksu); color:white; border:none; font-weight:700; cursor:pointer; }

  footer{ text-align:center; margin-top:26px; color:#8b5e3c; font-size:14px; }

  @media (max-width:680px){
    .hero{ flex-direction:column; align-items:flex-start; gap:12px; padding:12px; }
    .cart-bar{ left:50%; transform:translateX(-50%); right:auto; bottom:12px; width:94%; }
  }
</style>
</head>
<body>

<header>
  <h1>Elza's Whip</h1>
  <p>Whipped dreams • Cookies • Es Krim • Puding — coksu pastel vibes</p>
  <p class="address">📍 Jl. Pamujian Pasar 5, Karang Anyer</p>
  <p class="address">📱 WhatsApp: +6283857610717</p>
</header>

<main class="wrap" style="max-width:1100px;margin:0 auto;">
  <section class="hero" aria-label="intro">
    <div class="left">
      <h2>Menu Favorit 🍨</h2>
      <p>Pilih manisnya, tambahkan ke keranjang, dan checkout. 🍰💖</p>
    </div>
  </section>

  <section class="grid" id="menu"></section>

  <footer>
    © 2025 Elza's Whip — Manisnya bikin bahagia 💖
  </footer>
</main>

<div class="cart-bar" id="cartBar" aria-live="polite">
  <div class="cart-title">
    <div>Keranjang</div>
    <div style="font-size:13px;color:#6b4a3a" id="itemCount">0 item</div>
  </div>
  <div class="cart-list" id="cartList"></div>
  <div style="margin-bottom:8px; color:#6b4a3a; font-size:13px;">
    Total: <span style="font-weight:700;color:#8b4f2a">Rp <span id="totalPrice">0</span></span>
  </div>
  <div class="cart-footer">
    <button class="btn secondary" id="clearCart">Kosongkan</button>
    <button class="checkout" id="checkoutBtn">Checkout</button>
  </div>
</div>

<script>
const products = [
  {
    id:'1',
    name:'Strawberry Whip Sundae',
    desc:'Es krim stroberi lembut dengan whipped cream dan sprinkles. Varian pastel terfavorit!',
    price:18000,
    // Gambar Sundae Stroberi yang Aesthetic
    img:'https://images.unsplash.com/photo-1549419163-f018e6146c98?q=80&w=1200&auto=format&fit=crop' 
  },
  {
    id:'2',
    name:'Choco Crunch Cookie',
    desc:'Cookie cokelat hangat dengan choco chip lumer. Hangat, lembut, dan meleleh di mulut! 🍪',
    price:20000,
    // Gambar Cookie Cokelat
    img:'https://images.unsplash.com/photo-1558299863-c79234812328?q=80&w=1200&auto=format&fit=crop' 
  },
  {
    id:'3',
    name:'Vanilla Dream Puff',
    desc:'Puff vanilla lembut dengan sirup karamel manis. Diisi dengan krim vanila manis ringan. 🍯',
    price:22000,
    // Gambar Cream Puff/Eclair
    img:'https://images.unsplash.com/photo-1621939106297-759247d0e49f?q=80&w=1200&auto=format&fit=crop' 
  },
  {
    id:'4',
    name:'Matcha Cloud Ice Cream',
    desc:'Es krim matcha halus dengan topping mochi dan white choco. Rasa Matcha yang creamy dan menenangkan. 🍵',
    price:23000,
    // Gambar Matcha Ice Cream / Dessert Hijau Pastel
    img:'https://images.unsplash.com/photo-1551745455-89b52a7c4193?q=80&w=1200&auto=format&fit=crop' 
  }
];

const menu=document.getElementById('menu');
function formatRp(n){return new Intl.NumberFormat('id-ID').format(n)}
let cart={};
function updateCartUI(){
  const list=document.getElementById('cartList');
  const totalEl=document.getElementById('totalPrice');
  const itemCount=document.getElementById('itemCount');
  list.innerHTML=''; let total=0; let count=0;
  for(const id in cart){
    const p=products.find(x=>x.id===id);
    const q=cart[id]; total+=p.price*q; count+=q;
    const item=document.createElement('div');
    item.className='cart-item';
    item.innerHTML=`<img src="${p.img}" alt="">
    <div class="meta"><div class="n">${p.name}</div><div>Rp ${formatRp(p.price)} × ${q}</div></div>
    <div class="qty">${q}</div>`;
    list.appendChild(item);
  }
  totalEl.textContent=formatRp(total);
  itemCount.textContent=count+' item';
}

products.forEach(p=>{
  const div=document.createElement('div');
  div.className='card';
  div.innerHTML=`
  <a class="imgwrap" href="#"><img src="${p.img}" alt="${p.name}"></a>
  <div class="card-body">
  <div class="title">${p.name}</div>
  <div class="desc">${p.desc}</div>
  <div class="price">Rp ${formatRp(p.price)}</div>
  <button class="btn" onclick="addCart('${p.id}')">Tambah ke Keranjang</button>
  </div>`;
  menu.appendChild(div);
});
function addCart(id){cart[id]=(cart[id]||0)+1;updateCartUI();}
document.getElementById('clearCart').onclick=()=>{cart={};updateCartUI();}
document.getElementById('checkoutBtn').onclick=()=>{
  if(Object.keys(cart).length===0){alert('Keranjang masih kosong 🛒');return;}
  let pesan='Halo Elza! Saya mau pesan:\n';
  let total=0;
  for(const id in cart){
    const p=products.find(x=>x.id===id);
    const q=cart[id];
    pesan+=`- ${p.name} x${q}\n`;
    total+=p.price*q;
  }
  pesan+=`\nTotal: Rp ${formatRp(total)}\nAlamat: Jl. Pamujian Pasar 5, Karang Anyer`;
  window.open(`https://wa.me/6283857610717?text=${encodeURIComponent(pesan)}`);
};
updateCartUI();
</script>
</body>
</html>
