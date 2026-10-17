<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>M. Yousaf Cloth House</title>

  <style>
    :root {
      --black: #171512;
      --beige: #e9dfcf;
      --cream: #faf7f1;
      --brown: #776653;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: Arial, sans-serif;
      background: var(--cream);
      color: var(--black);
    }

    header {
      background: var(--beige);
      padding: 16px 5%;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .logo {
      width: 58px;
      height: 58px;
      object-fit: contain;
    }

    .brand h1 {
      font-size: 21px;
    }

    nav {
      display: flex;
      gap: 22px;
      overflow-x: auto;
      padding-top: 18px;
    }

    nav a {
      color: var(--black);
      text-decoration: none;
      white-space: nowrap;
      font-size: 14px;
    }

    .banner {
      background: var(--black);
      color: var(--beige);
      text-align: center;
      padding: 55px 20px;
    }

    .banner img {
      width: 120px;
      height: 120px;
      object-fit: contain;
      margin-bottom: 15px;
    }

    .banner h2 {
      font-size: 29px;
      margin-bottom: 12px;
    }

    .banner p {
      color: #e9dfcf;
      line-height: 1.6;
    }

    section {
      padding: 38px 5%;
    }

    .section-title {
      text-align: center;
      margin-bottom: 25px;
    }

    .section-title h2 {
      font-size: 25px;
      margin-bottom: 8px;
    }

    .section-title p {
      color: var(--brown);
      font-size: 14px;
    }

    .products {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 14px;
    }

    .product {
      background: white;
      border: 1px solid #e5dac9;
      padding: 10px;
      border-radius: 8px;
    }

    .product-gallery {
      display: flex;
      gap: 6px;
      overflow-x: auto;
      scroll-snap-type: x mandatory;
    }

    .product-gallery img {
      width: 100%;
      min-width: 100%;
      height: 180px;
      object-fit: cover;
      scroll-snap-align: start;
      cursor: pointer;
      border-radius: 5px;
    }

    .product h3 {
      font-size: 16px;
      margin-top: 13px;
    }

    .price {
      font-weight: bold;
      margin: 8px 0;
    }

    .description {
      font-size: 13px;
      line-height: 1.5;
      color: var(--brown);
    }

    .order-button {
      display: block;
      background: var(--black);
      color: white;
      text-align: center;
      padding: 11px 5px;
      border-radius: 5px;
      text-decoration: none;
      font-size: 13px;
      margin-top: 12px;
    }

    .how-to-order {
      background: var(--beige);
      text-align: center;
      line-height: 1.9;
    }

    footer {
      background: var(--black);
      color: var(--beige);
      padding: 28px 15px;
      text-align: center;
      line-height: 1.8;
      font-size: 14px;
    }

    .lightbox {
      display: none;
      position: fixed;
      inset: 0;
      background: rgba(0, 0, 0, 0.94);
      z-index: 10;
      align-items: center;
      justify-content: center;
      padding: 20px;
    }

    .lightbox img {
      max-width: 95%;
      max-height: 80vh;
      object-fit: contain;
    }

    .lightbox button {
      position: absolute;
      top: 20px;
      right: 20px;
      padding: 10px 14px;
      font-size: 18px;
    }

    @media (max-width: 360px) {
      .product-gallery img {
        height: 140px;
      }

      .brand h1 {
        font-size: 17px;
      }
    }
  </style>
</head>

<body>

  <header id="home">
    <div class="brand">
      <!-- Add your logo file here later -->
      <img class="logo" src="logo.png" alt="M. Yousaf Cloth House logo">
      <h1>M. Yousaf Cloth House</h1>
    </div>

    <nav>
      <a href="#home">Home</a>
      <a href="#products">Collection</a>
      <a href="#how-to-order">How to Order</a>
      <a href="#about">About Us</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <main>
    <div class="banner">
      <img src="logo.png" alt="M. Yousaf Cloth House logo">
      <h2>M. Yousaf Cloth House</h2>
      <p>Discover Our Collection</p>
    </div>

    <section id="products">
      <div class="section-title">
        <h2>Our Collection</h2>
        <p>Explore our latest styles</p>
      </div>

      <div class="products">

        <!-- Copy this product card to add more products -->
        <article class="product">
          <div class="product-gallery">
            <img src="product1.jpg" alt="Product photo 1"
                 onclick="openPhoto(this.src)">
            <img src="product1-2.jpg" alt="Product photo 2"
                 onclick="openPhoto(this.src)">
          </div>

          <h3>Product Name</h3>
          <p class="price">Price: Rs. 0</p>
          <p class="description">
            Your product description will appear here.
          </p>

          <a class="order-button"
             href="https://wa.me/923001234567?text=I%20want%20to%20order%20Product%20Name">
            WhatsApp Order
          </a>

          <a class="order-button"
             href="https://wa.me/923001234567">
            WhatsApp Chat
          </a>
        </article>

        <article class="product">
          <div class="product-gallery">
            <img src="product2.jpg" alt="Product photo 1"
                 onclick="openPhoto(this.src)">
            <img src="product2-2.jpg" alt="Product photo 2"
                 onclick="openPhoto(this.src)">
          </div>

          <h3>Product Name</h3>
          <p class="price">Price: Rs. 0</p>
          <p class="description">
            Your product description will appear here.
          </p>

          <a class="order-button"
             href="https://wa.me/923001234567?text=I%20want%20to%20order%20Product%20Name">
            WhatsApp Order
          </a>

          <a class="order-button"
             href="https://wa.me/923001234567">
            WhatsApp Chat
          </a>
        </article>

      </div>
    </section>

    <section id="how-to-order" class="how-to-order">
      <div class="section-title">
        <h2>How to Order</h2>
        <p>Choose your favorite product and contact us on WhatsApp.</p>
      </div>
      <p>1. Browse our collection.</p>
      <p>2. Select the product you love.</p>
      <p>3. Tap WhatsApp Order to contact us.</p>
    </section>

    <section id="about">
      <div class="section-title">
        <h2>About Us</h2>
        <p>Welcome to M. Yousaf Cloth House.</p>
      </div>
    </section>
  </main>

  <footer id="contact">
    <h2>M. Yousaf Cloth House</h2>
    <p>For orders and inquiries, contact us on WhatsApp.</p>
    <p>©️ M. Yousaf Cloth House</p>
  </footer>

  <div class="lightbox" id="lightbox"
       onclick="if(event.target === this) closePhoto()">
    <button onclick="closePhoto()">Close ✕</button>
    <img id="largePhoto" src="" alt="Enlarged product">
  </div>

  <script>
    function openPhoto(src) {
      document.getElementById("largePhoto").src = src;
      document.getElementById("lightbox").style.display = "flex";
    }

    function closePhoto() {
      document.getElementById("lightbox").style.display = "none";
    }
  </script>

</body>
</html>
