# VAIS-COLLECTION
VAIS COLLECTION — Island-inspired fashion &amp; jewellery:dresses, pearl necklaces, rings &amp; more.
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>VAIS COLLECTION</title>

<link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" rel="stylesheet">

<style>
body{margin:0;font-family:'Segoe UI',sans-serif;background:#0a0a0a;color:white;}
header{display:flex;justify-content:space-between;padding:20px 40px;background:black;position:sticky;top:0;z-index:1000;}
header h1{color:gold;letter-spacing:2px;}
nav a{color:white;margin:0 15px;text-decoration:none;font-weight:500;}
nav a:hover{color:gold;}
.hero{height:80vh;background:url('https://images.unsplash.com/photo-1603974372039-adc49044b6bd') center/cover no-repeat;display:flex;align-items:center;justify-content:center;text-align:center;}
.hero h2{font-size:50px;margin:0;}
.hero p{font-size:20px;opacity:0.8;}
section{padding:50px 20px;}
h2{color:gold;text-align:center;margin-bottom:40px;}
.shop-container{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:20px;justify-items:center;}
.product{background:#1a1a1a;padding:20px;border-radius:12px;text-align:center;width:200px;}
.product img{width:100%;border-radius:10px;}
.product button{margin-top:10px;padding:10px;background:gold;color:black;font-weight:bold;border:none;cursor:pointer;border-radius:5px;}
.blog-container{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:20px;}
.blog-post{background:#222;padding:20px;border-radius:10px;}
form input,form textarea{width:100%;padding:12px;margin:10px 0;border-radius:5px;border:none;}
form button{background:gold;padding:12px 20px;border:none;cursor:pointer;font-weight:bold;color:black;border-radius:5px;}
.cart{position:fixed;right:0;top:0;width:300px;height:100%;background:#111;padding:20px;overflow-y:auto;z-index:999;}
.cart h3{color:gold;margin-top:0;}
.cart ul{list-style:none;padding:0;}
.cart li{padding:8px 0;border-bottom:1px solid #333;}
.cart p{font-weight:bold;}
footer{text-align:center;padding:20px;background:black;margin-top:50px;}
</style>
</head>

<body>
<header>
<h1>VAIS COLLECTION</h1>
<nav>
<a href="#home">Home</a>
<a href="#shop">Shop</a>
<a href="#blog">Blog</a>
<a href="#contact">Contact</a>
</nav>
</header>

<div class="hero" id="home">
<div>
<h2>VAIS COLLECTION</h2>
<p>Island Luxury Jewellery & Accessories</p>
</div>
</div>

<section id="shop">
<h2>Shop</h2>
<div class="shop-container">

<div class="product">
<img src="https://images.unsplash.com/photo-1617038220319-276d3cfab638" alt="Gold Chain">
<h3>Gold Chain</h3>
<p>$50</p>
<button onclick="addToCart('Gold Chain',50)">Add to Cart</button>
</div>

<div class="product">
<img src="https://images.unsplash.com/photo-1613999532486-93d5b7a7d3d6" alt="Diamond Ring">
<h3>Diamond Ring</h3>
<p>$90</p>
<button onclick="addToCart('Diamond Ring',90)">Add to Cart</button>
</div>

<div class="product">
<img src="https://images.unsplash.com/photo-1613999552733-7f5c0d1b9324" alt="Bracelet">
<h3>Bracelet</h3>
<p>$40</p>
<button onclick="addToCart('Bracelet',40)">Add to Cart</button>
</div>

</div>
</section>

<section id="blog">
<h2>Blog</h2>
<div class="blog-container">
<div class="blog-post">
<h3>Styling Tips for Jewellery</h3>
<p>Learn how to elevate your look with premium jewellery.</p>
</div>
<div class="blog-post">
<h3>2026 Trends</h3>
<p>Discover the latest island-luxury fashion trends.</p>
</div>
<div class="blog-post">
<h3>Confidence & Style</h3>
<p>How your style speaks before you do.</p>
</div>
</div>
</section>

<section id="contact">
<h2>Contact</h2>
<form>
<input type="text" placeholder="Your Name" required>
<input type="email" placeholder="Your Email" required>
<textarea rows="5" placeholder="Message"></textarea>
<button type="submit">Send Message</button>
</form>
</section>

<div class="cart">
<h3>Cart</h3>
<ul id="cart-items"></ul>
<p>Total: $<span id="total">0</span></p>
<button onclick="checkout()">Checkout</button>
</div>

<footer>
<p>© 2026 VAIS COLLECTION</p>
</footer>

<script>
let cart=[];
let total=0;
function addToCart(name,price){cart.push({name,price});total+=price;updateCart();}
function updateCart(){const list=document.getElementById("cart-items");list.innerHTML="";cart.forEach(item=>{const li=document.createElement("li");li.textContent=item.name+" - $"+item.price;list.appendChild(li);});document.getElementById("total").textContent=total;}
function checkout(){alert("Checkout coming soon! Connect Stripe or PayPal to start selling.");}
</script>

</body>
</html>
