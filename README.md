<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>متجر زومبي الدمام</title>
<style>
  /* Reset */
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background: #0b0b0b;
    color: #eee;
    direction: rtl;
  }

  header {
    background: #1a1a1a;
    padding: 20px;
    text-align: center;
    border-bottom: 3px solid #d32020;
  }

  header h1 {
    font-size: 2.8rem;
    color: #d32020;
    text-shadow:
      0 0 8px #d32020,
      0 0 20px #9aff9a,
      0 0 30px #9aff9a,
      0 0 40px #d32020;
    letter-spacing: 4px;
  }

  .container {
    max-width: 1100px;
    margin: 30px auto;
    padding: 0 15px;
  }

  .products {
    display: grid;
    grid-template-columns: repeat(auto-fit,minmax(220px,1fr));
    gap: 25px;
  }

  .product {
    background: #1c1c1c;
    border: 2px solid #333;
    border-radius: 8px;
    padding: 15px;
    box-shadow: 0 0 12px #d32020aa;
    transition: transform 0.3s ease;
  }

  .product:hover {
    transform: scale(1.05);
    border-color: #9aff9a;
    box-shadow: 0 0 20px #9aff9aaa;
  }

  .product img {
    width: 100%;
    border-radius: 5px;
  }

  .product h3 {
    margin: 15px 0 10px;
    color: #d32020;
    font-size: 1.3rem;
  }

  .product p {
    font-size: 0.95rem;
    color: #bbb;
    height: 45px;
    overflow: hidden;
  }

  .product .price {
    margin: 10px 0;
    font-weight: bold;
    color: #9aff9a;
    font-size: 1.1rem;
  }

  .product button {
    background: #d32020;
    border: none;
    color: #eee;
    padding: 10px 15px;
    font-size: 1rem;
    border-radius: 6px;
    cursor: pointer;
    transition: background 0.25s ease;
  }

  .product button:hover {
    background: #9aff9a;
    color: #111;
  }

  .cart {
    position: fixed;
    top: 20px;
    left: 20px;
    background: #d32020;
    color: #eee;
    padding: 10px 18px;
    border-radius: 50px;
    font-weight: bold;
    box-shadow: 0 0 10px #d32020aa;
    cursor: pointer;
    user-select: none;
    z-index: 1000;
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .cart:hover {
    background: #9aff9a;
    color: #111;
  }

  .cart span {
    font-size: 1.2rem;
  }

  /* Responsive */
  @media (max-width: 600px) {
    header h1 {
      font-size: 2rem;
    }

    .product h3 {
      font-size: 1.1rem;
    }

    .product p {
      height: auto;
    }
  }
</style>
</head>
<body>

<header>
  <h1>زومبي الدمام</h1>
</header>

<div class="container">
  <div class="products">

    <div class="product">
      <img src="https://i.imgur.com/UGVFpRO.jpg" alt="سلاح بلازما" />
      <h3>سلاح بلازما</h3>
      <p>سلاح متقدم لمواجهة الزومبي بفعالية عالية.</p>
      <div class="price">150 دمام كوينز</div>
      <button class="add-to-cart">أضف إلى السلة</button>
    </div>

    <div class="product">
      <img src="https://i.imgur.com/y7hU6ZQ.jpg" alt="خوذة واقية" />
      <h3>خوذة واقية</h3>
      <p>خوذة تحمي رأسك من هجمات الزومبي.</p>
      <div class="price">80 دمام كوينز</div>
      <button class="add-to-cart">أضف إلى السلة</button>
    </div>

    <div class="product">
      <img src="https://i.imgur.com/DeuGQzM.jpg" alt="زجاجة مضادة للسموم" />
      <h3>زجاجة مضادة للسموم</h3>
      <p>تقي نفسك من السموم الفيروسية.</p>
      <div class="price">50 دمام كوينز</div>
      <button class="add-to-cart">أضف إلى السلة</button>
    </div>

    <div class="product">
      <img src="https://i.imgur.com/5QhTYYf.jpg" alt="حزام ذخيرة" />
      <h3>حزام ذخيرة</h3>
      <p>زيادة سعة الذخيرة الخاصة بك.</p>
      <div class="price">100 دمام كوينز</div>
      <button class="add-to-cart">أضف إلى السلة</button>
    </div>

    <div class="product">
      <img src="https://i.imgur.com/GzLmJaC.jpg" alt="قفازات قتالية" />
      <h3>قفازات قتالية</h3>
      <p>تعزز من قوة ضرباتك ضد الزومبي.</p>
      <div class="price">90 دمام كوينز</div>
      <button class="add-to-cart">أضف إلى السلة</button>
    </div>

  </div>
</div>

<div class="cart" title="عربة التسوق">
  🛒 السلة: <span id="cart-count">0</span>
</div>

<script>
  const cartCount = document.getElementById('cart-count');
  const buttons = document.querySelectorAll('.add-to-cart');

  let count = 0;

  buttons.forEach(button => {
    button.addEventListener('click', () => {
      count++;
      cartCount.textContent = count;
      // يمكن هنا تضيف تخزين محلي أو تنبيه
      alert('تم إضافة المنتج إلى السلة!');
    });
  });
</script>

</body>
</html>
