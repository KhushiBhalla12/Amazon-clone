# Amazon-clone
🛍️ Amazon Clone A full-featured eCommerce web application inspired by Amazon, built using HTML, CSS, JavaScript, and localStorage. This project simulates real-world shopping functionality including product listing, cart management, user authentication, admin dashboard, and order tracking.
<!DOCTYPE html>
<html lang="en">
<head>

  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Amazon Clone</title>
  <header class="top-navbar">
  <div class="top-row">
    <div class="logo">amazon<span>.in</span></div>
    <div class="delivery">
      <span>Delivering to Kolkata 700047</span><br>
      <strong>Update location</strong>
      
    </div>
    <div class="search-container">
      <select>
        <option>All</option>
        <option>Electronics</option>
        <option>Books</option>
        <option>Fashion</option>
        <option>Baby</option>
        <option>Beauty & Personal Care </option>
        <option>Computer</option>
        <option>Sports & Outdoor</option>
        <option>Kindle store</option>
        <option>Deals</option>
        <option>Digital music</option>
        <option>Video games</option>
        <option>Toys and games</option>
        <option>Home and kitchen </option>
        <option>Health and household </option>
        <option>Music and CDs </option>
        <option>Automotives </option>
        <option>art and craft</option>
      </select>
      <input type="text" placeholder="Search Amazon.in">
      <button class="search-btn"> 🔍</button>
    </div>
    <div class="nav-icons">
  <div class="lang-toggle" onclick="toggleLangDropdown()">🇮🇳 EN ▼</div>
  <div class="lang-menu" id="langMenu">
    <label><input type="radio" name="lang" checked> English - EN</label>
    <label><input type="radio" name="lang"> हिन्दी - HI</label>
    <label><input type="radio" name="lang"> தமிழ் - TA</label>
    <label><input type="radio" name="lang"> తెలుగు - TE</label>
    <label><input type="radio" name="lang"> ಕನ್ನಡ - KN</label>
    <label><input type="radio" name="lang"> മലയാളം - ML</label>
    <label><input type="radio" name="lang"> বাংলা - BN</label>
    <label><input type="radio" name="lang"> मराठी - MR</label>
    <hr>
    <a href="#">Learn more</a>
    <div class="region-info">
      🇮🇳 You are shopping on Amazon.in<br>
      <a href="#">Change country/region</a>
    </div>
  </div>
</div>


      <div class="account-dropdown">
  <div class="account-toggle" onclick="toggleAccountMenu()">Hello, sign in<br><strong>Account & Lists ▼</strong></div>
  <div class="account-menu" id="accountMenu">
    <div class="account-signin">
      <button>Sign in</button>
      <p>New customer? <a href="#">Start here.</a></p>
    </div>
    <hr />
    <div class="account-columns">
      <div>
        <h4>Your Lists</h4>
        <ul>
          <li>Create a Wish List</li>
          <li>Wish from Any Website</li>
          <li>Baby Wishlist</li>
          <li>Discover Your Style</li>
          <li>Explore Showroom</li>
        </ul>
      </div>
      <div>
        <h4>Your Account</h4>
        <ul>
          <li>Your Account</li>
          <li>Your Orders</li>
          <li>Your Wish List</li>
          <li>Your Recommendations</li>
          <li>Your Prime Membership</li>
          <li>Your Prime Video</li>
          <li>Your Subscribe & Save Items</li>
          <li>Memberships & Subscriptions</li>
          <li>Your Seller Account</li>
          <li>Manage Your Content and Devices</li>
          <li>Register for a free Business Account</li>
        </ul>
      </div>
    </div>
  </div>
</div>

      <div class="orders">Returns<br><strong>& Orders</strong></div>
    <a href="cart.html" id="cartLink">Cart 🛒</a>

    </div>
  </div>

  <div class="bottom-row">
    <a href="#">☰ All</a>
    <a href="#">Fresh</a>
    <a href="#">MX Player</a>
    <a href="#">Sell</a>
    <a href="#">Bestsellers</a>
    <a href="#">Today's Deals</a>
    <a href="#">Mobiles</a>
    <a href="#">Prime</a>
    <a href="#">Customer Service</a>
    <a href="#">New Releases</a>
    <a href="#">Fashion</a>
    <a href="#">Amazon Pay</a>
    <a href="#">Electronics</a>
    <a href="#">Home & Kitchen</a>
    <a href="#">Computers</a>
    <a href="#">Books</a>
    <a href="#">Car & Motorbike</a>
  </div>
</header>


  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(to bottom, #e3e6e6, #f3f3f3);
    }
    .navbar {
        
      display: flex;
      align-items: center;
      justify-content: space-between;
      background-color: #131921;
      padding: 12px 20px;
      color: white;
    }
    
    .logo {
      font-size: 24px;
      font-weight: bold;
    }
    .logo span {
      color: #ff9900;
    }
    .search-bar {
      flex: 1;
      margin: 0 20px;
      display: flex;
    }
    .search-bar input {
      flex: 1;
      padding: 10px;
      border: none;
    }
    .search-bar button {
      padding: 8px 16px;
      background-color: #febd69;
      border: none;
      cursor: pointer;
    }
    .top-navbar {
  font-family: Arial, sans-serif;
  background-color: #131921;
  color: white;
}
.lang-dropdown {
  position: relative;
  cursor: pointer;
  font-size: 13px;
  display: inline-block;
}

.lang-toggle {
  padding: 5px;
}

.lang-menu {
  display: none;
  position: absolute;
  top: 32px;
  right: 20%;
  background-color: white;
  color: black;
  border: 1px solid #ccc;
  width: 250px;
  box-shadow: 0 2px 10px rgba(0,0,0,0.2);
  z-index: 9999;
  border-radius: 4px;
  padding: 10px;
}

.lang-menu label {
  display: block;
  margin-bottom: 5px;
  font-size: 14px;
  cursor: pointer;
}
.lang-menu hr {
  margin: 10px 0;
}
.lang-menu a {
  color: #0066c0;
  text-decoration: none;
  font-size: 13px;
}
.region-info {
  margin-top: 10px;
  font-size: 13px;
}
.region-info a {
  color: #0066c0;
}


.top-row {
  display: flex;
  align-items: center;
  padding: 10px 20px;
  gap: 20px;
}

.logo {
  font-size: 24px;
  font-weight: bold;
}
.logo span {
  color: #ff9900;
}

.delivery {
  font-size: 12px;
  line-height: 1.2;
}

.search-container {
  flex: 1;
  display: flex;
  max-width: 600px;
}
.search-container select {
  padding: 6px;
  border: none;
}
.search-container input {
  flex: 1;
  padding: 6px;
  border: none;
}
.search-btn {
  background-color: #febd69;
  border: none;
  padding: 6px 10px;
  cursor: pointer;
}

.nav-icons {
  display: flex;
  gap: 20px;
  font-size: 12px;
  align-items: center;
}
.nav-icons div strong {
  font-size: 13px;
  display: block;
}

.bottom-row {
  background-color: #232f3e;
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  padding: 10px 20px;
  font-size: 14px;
}
.bottom-row a {
  color: white;
  text-decoration: none;
}
.bottom-row a:hover {
  text-decoration: underline;
}

    .cart {
      font-size: 18px;
      cursor: pointer;
    }
    .amazon-carousel {
      position: relative;
      width: 100%;
      max-height: 400px;
      overflow: hidden;
      margin-bottom: 20px;
    }
    .carousel-wrapper {
      position: relative;
      width: 100%;
      height: 400px;
    }
    .banner-slide {
      position: absolute;
      width: 100%;
      height: 100%;
      object-fit: cover;
      object-position: center;
      opacity: 0;
      transition: opacity 1s ease-in-out;
      z-index: 0;
      display: block;
    }
    .banner-slide.active {
      opacity: 1;
      z-index: 1;
    }
    .carousel-btn {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      font-size: 36px;
      background: rgba(0,0,0,0.4);
      color: white;
      border: none;
      cursor: pointer;
      padding: 10px 16px;
      z-index: 2;
    }
    .carousel-btn.prev {
      left: 10px;
    }
    .carousel-btn.next {
      right: 10px;
    }
    .carousel-dots {
      position: absolute;
      bottom: 15px;
      left: 50%;
      transform: translateX(-50%);
      display: flex;
      gap: 8px;
      z-index: 2;
    }
    .carousel-dots span {
      width: 12px;
      height: 12px;
      border-radius: 50%;
      background-color: rgba(255, 255, 255, 0.6);
      cursor: pointer;
      transition: background-color 0.3s;
    }
    .carousel-dots span.active {
      background-color: #ffffff;
    }
    .section-title {
      padding: 10px 20px;
      font-size: 20px;
      font-weight: bold;
    }
    .products {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 20px;
      padding: 20px;
    }
    .product {
      background: white;
      border-radius: 8px;
      padding: 12px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
      transition: transform 0.2s, box-shadow 0.2s;
      position: relative;
    }
    .product:hover {
      transform: translateY(-5px);
      box-shadow: 0 4px 12px rgba(0,0,0,0.2);
    }
    .product img {
      width: 100%;
      height: 160px;
      object-fit: contain;
    }
    .product h3 {
      font-size: 16px;
      margin: 10px 0 4px;
    }
    .product p {
      margin-bottom: 10px;
      font-weight: bold;
    }
    .old-price {
      text-decoration: line-through;
      color: gray;
      font-weight: normal;
    }
    .badge {
      background: gold;
      padding: 2px 6px;
      font-size: 12px;
      position: absolute;
      top: 8px;
      left: 8px;
      border-radius: 3px;
    }
    .product button {
      padding: 6px 10px;
      background-color: #ffd814;
      border: none;
      cursor: pointer;
      width: 100%;
      font-weight: bold;
    }
    .prime-banner {
      background: url('assets/prime-banner.jpg') no-repeat center center;
      background-size: cover;
      height: 220px;
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      margin-top: 40px;
      position: relative;
      text-align: center;
    }
    .prime-banner::after {
      content: '';
      position: absolute;
      inset: 0;
      background: rgba(0, 0, 0, 0.6);
    }
    .prime-content {
      position: relative;
      z-index: 2;
    }
    .prime-content h2 {
      font-size: 24px;
      margin-bottom: 8px;
    }
    .prime-content p {
      font-size: 16px;
      margin-bottom: 12px;
    }
    .prime-btn {
      display: inline-block;
      padding: 10px 18px;
      background-color: #ffd814;
      color: #111;
      font-weight: bold;
      text-decoration: none;
      border-radius: 4px;
    }
    .footer {
  background-color: #232f3e;
  color: #fff;
  padding: 30px 20px 10px;
  font-size: 14px;
}
.footer-columns {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  gap: 20px;
  margin-bottom: 20px;
}
.footer-columns h4 {
  margin-bottom: 10px;
  color: #fff;
}
.footer-columns ul {
  list-style: none;
  padding: 0;
}
.footer-columns li {
  margin-bottom: 6px;
  cursor: pointer;
  color: #ddd;
}
.footer-columns li:hover {
  text-decoration: underline;
}
.footer-bottom {
  text-align: center;
  border-top: 1px solid #444;
  padding-top: 10px;
  color: #aaa;
}
.account-dropdown {
  position: relative;
  display: inline-block;
  color: white;
  font-size: 13px;
  cursor: pointer;
}

.account-menu {
  display: none;
  position: absolute;
  top: 100%;
  right: 0;
  width: 550px;
  background-color: white;
  color: #111;
  box-shadow: 0 2px 12px rgba(0,0,0,0.2);
  z-index: 1000;
  padding: 20px;
  border-radius: 4px;
}

.account-signin {
  text-align: center;
  margin-bottom: 10px;
}
.account-signin button {
  background-color: #ffd814;
  border: none;
  padding: 8px 20px;
  font-weight: bold;
  cursor: pointer;
  border-radius: 4px;
}
.account-signin p {
  font-size: 13px;
  margin-top: 8px;
}
.account-signin a {
  color: #007185;
  text-decoration: none;
}

.account-columns {
  display: flex;
  gap: 30px;
}
.account-columns h4 {
  font-size: 15px;
  margin-bottom: 10px;
}
.account-columns ul {
  list-style: none;
  padding: 0;
}
.account-columns li {
  font-size: 13px;
  margin-bottom: 6px;
  cursor: pointer;
}
.account-columns li:hover {
  text-decoration: underline;
}

  </style>
</head>
<body>
  <header class="navbar">
  </header>
  <div class="amazon-carousel" id="carousel">
    <div class="carousel-wrapper">
      <img src="assets/banner.jpg" class="banner-slide active" alt="Banner 1">
      <img src="assets/banner1.jpg" class="banner-slide" alt="Banner 2">
      <img src="assets/banner2.jpg" class="banner-slide" alt="Banner 3">
    </div>
    <button class="carousel-btn prev" onclick="prevSlide()">❮</button>
    <button class="carousel-btn next" onclick="nextSlide()">❯</button>
    <div class="carousel-dots" id="carouselDots"></div>
  </div>

  <h2 class="section-title">Top Deals</h2>
  <section class="products" id="productsContainer"></section>

  <div class="prime-banner">
    <div class="prime-content">
      <h2>Enjoy unlimited FREE fast delivery with Amazon Prime</h2>
      <p>Also get access to the latest movies, TV shows & more</p>
      <a href="#" class="prime-btn">Join Prime</a>
    </div>
  </div>

  <script>
    const products = [
      { id: 1, name: "Wireless Headphones", price: 1499, oldPrice: 1999, image: "assets/headphones.jpg", badge: "Best Seller" },
      { id: 2, name: "Bluetooth Speaker", price: 999, oldPrice: 1299, image: "assets/speaker.jpg", badge: "Top Rated" },
      { id: 3, name: "Smartphone Case", price: 299, oldPrice: 399, image: "assets/case.jpg" },
      { id: 4, name: "Laptop Stand", price: 899, oldPrice: 1299, image: "assets/stand.jpg" },
      { id: 5, name: "Gaming Mouse", price: 1299, oldPrice: 1599, image: "assets/mouse.jpg" },
      { id: 6, name: "Fitness Smartwatch", price: 2499, oldPrice: 2999, image: "assets/watch.jpg", badge: "Limited Offer" },
      { id: 7, name: "Smart LED Bulb", price: 699, oldPrice: 899, image: "assets/bulb.jpg" },
      { id: 8, name: "Tablet Stand", price: 499, oldPrice: 799, image: "assets/stand2.jpg" }
    ];
    function loadProducts(list) {
  const container = document.getElementById("productsContainer");
  container.innerHTML = ""; // Clear previous content if any

  list.forEach(product => {
    const productHTML = `
      <div class="product">
        ${product.badge ? `<span class="badge">${product.badge}</span>` : ""}
        <img src="${product.image}" alt="${product.name}">
        <h3>${product.name}</h3>
        <p><span class="old-price">₹${product.oldPrice}</span> ₹${product.price}</p>
        <div class="rating">⭐⭐⭐⭐☆ (215)</div>
        <button onclick="addToCart(${product.id})">Add to Cart</button>
      </div>
    `;

    container.innerHTML += productHTML;
  });
}

    function searchProducts() {
      const query = document.getElementById("searchInput").value.toLowerCase();
      const filtered = products.filter(p => p.name.toLowerCase().includes(query));
      loadProducts(filtered);
    }

    function addToCart(id) {
  let cart = JSON.parse(localStorage.getItem("cart")) || [];
  const item = products.find(p => p.id === id);
  const existing = cart.find(p => p.id === id);

  if (existing) {
    existing.quantity += 1;
  } else {
    cart.push({ ...item, quantity: 1 });
  }

  localStorage.setItem("cart", JSON.stringify(cart));
  alert(`Added ${item.name} to cart!`);
}


    const slides = document.querySelectorAll(".banner-slide");
    const dotsContainer = document.getElementById("carouselDots");
    const carousel = document.getElementById("carousel");
    let currentIndex = 0;
    let slideInterval;

    slides.forEach((_, idx) => {
      const dot = document.createElement("span");
      dot.addEventListener("click", () => goToSlide(idx));
      dotsContainer.appendChild(dot);
    });

    const dots = dotsContainer.querySelectorAll("span");

    function showSlide(index) {
      slides.forEach((slide, i) => {
        slide.classList.toggle("active", i === index);
      });
      dots.forEach((dot, i) => {
        dot.classList.toggle("active", i === index);
      });
    }

    function nextSlide() {
      currentIndex = (currentIndex + 1) % slides.length;
      showSlide(currentIndex);
    }

    function prevSlide() {
      currentIndex = (currentIndex - 1 + slides.length) % slides.length;
      showSlide(currentIndex);
    }

    function goToSlide(index) {
      currentIndex = index;
      showSlide(currentIndex);
    }

    function startAutoSlide() {
      slideInterval = setInterval(nextSlide, 4000);
    }

    function stopAutoSlide() {
      clearInterval(slideInterval);
    }

    window.onload = () => {
      showSlide(currentIndex);
      startAutoSlide();
      if (document.getElementById("productsContainer")) {
        loadProducts(products);
      }
      carousel.addEventListener("mouseenter", stopAutoSlide);
      carousel.addEventListener("mouseleave", startAutoSlide);
    };
    function toggleLangDropdown() {
  const menu = document.getElementById("langMenu");
  menu.style.display = menu.style.display === "block" ? "none" : "block";
}

window.addEventListener("click", function(e) {
  const langDropdown = document.querySelector(".lang-dropdown");
  if (!langDropdown.contains(e.target)) {
    document.getElementById("langMenu").style.display = "none";
  }
});
function toggleAccountMenu() {
  const menu = document.getElementById("accountMenu");
  menu.style.display = menu.style.display === "block" ? "none" : "block";
}

window.addEventListener("click", function (e) {
  const accountDropdown = document.querySelector(".account-dropdown");
  if (!accountDropdown.contains(e.target)) {
    document.getElementById("accountMenu").style.display = "none";
  }
});


  </script>
  <footer class="footer">
  <div class="footer-columns">
    <div>
      <h4>Get to Know Us</h4>
      <ul>
        <li>About Us</li>
        <li>Careers</li>
        <li>Press Releases</li>
        <li>Amazon Science</li>
      </ul>
    </div>
    <div>
      <h4>Connect with Us</h4>
      <ul>
        <li>Facebook</li>
        <li>Twitter</li>
        <li>Instagram</li>
      </ul>
    </div>
    <div>
      <h4>Make Money with Us</h4>
      <ul>
        <li>Sell on Amazon</li>
        <li>Become an Affiliate</li>
        <li>Advertise Your Products</li>
        <li>Amazon Pay</li>
      </ul>
    </div>
    <div>
      <h4>Let Us Help You</h4>
      <ul>
        <li>Your Account</li>
        <li>Returns Centre</li>
        <li>100% Purchase Protection</li>
        <li>Help</li>
      </ul>
    </div>
  </div>
  <div class="footer-bottom">
    <p>© 2025 Amazon Clone. All rights reserved.</p>
  </div>
</footer>

</body>
</html> 

