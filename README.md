# Ex.07 Restaurant Website
## Date:

## AIM:
To develop a static Restaurant website to display the food items and services provided by them.

## DESIGN STEPS:

### Step 1:
Requirement collection.

### Step 2:
Creating the layout using HTML and CSS.

### Step 3:
Updating the sample content.

### Step 4:
Choose the appropriate style and color scheme.

### Step 5:
Validate the layout in various browsers.

### Step 6:
Validate the HTML code.

### Step 7:
Publish the website in the given URL.

## PROGRAM:
```
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>The royal bites- Restaurant</title>
  <style>
    body {
      margin: 0;
      font-family: 'Roboto', sans-serif;
      background: linear-gradient(135deg, #beb7bc 0%, #eeebed 100%);
      color: #070707;
      overflow-x: hidden;
    }
    header {
      background: url('1.jpg') no-repeat center center/cover;
      height: 400px;
      display: flex;
      align-items: center;
      justify-content: center;
      color: #050505;
      font-size: 60px;
      font-weight: bold;
      text-shadow: 4px 4px 12px rgba(246, 236, 236, 0.8);
      position: relative;
      animation: fadeIn 2s ease-in-out;
    }
    header::after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 0;
      right: 0;
      height: 120px;
      background: linear-gradient(to top, rgba(0,0,0,0.7), transparent);
    }
    header h1 {
      z-index: 1;
      animation: slideUp 1.5s ease-out;
    }
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
    @keyframes slideUp {
      from { transform: translateY(50px); opacity: 0; }
      to { transform: translateY(0); opacity: 1; }
    }
    nav {
      background: rgba(149, 15, 116, 0.9);
      padding: 20px 0;
      text-align: center;
      box-shadow: 0 4px 10px rgba(0,0,0,0.2);
      backdrop-filter: blur(10px);
    }
    nav a {
      color: #fff;
      margin: 0 30px;
      text-decoration: none;
      font-weight: bold;
      font-size: 20px;
      transition: all 0.4s ease;
      position: relative;
    }
    nav a::after {
      content: '';
      position: absolute;
      width: 0;
      height: 2px;
      bottom: -5px;
      left: 50%;
      background-color: #fff;
      transition: all 0.4s ease;
    }
    nav a:hover::after {
      width: 100%;
      left: 0;
    }
    nav a:hover {
      color: #ffd700;
      transform: scale(1.1);
    }
    section {
      padding: 80px 20px;
      max-width: 1200px;
      margin: 0 auto;
      text-align: center;
      animation: fadeInUp 1s ease-out;
    }
    @keyframes fadeInUp {
      from { opacity: 0; transform: translateY(30px); }
      to { opacity: 1; transform: translateY(0); }
    }
    section h2 {
      font-size: 48px;
      margin-bottom: 40px;
      color:#7e0556;
      border-bottom: 4px solid;
      display: inline-block;
      padding-bottom: 15px;
      text-shadow: 1px 1px 3px rgba(0,0,0,0.3);
    }
    .menu-grid, .admin-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
      gap: 40px;
      margin-top: 50px;
    }
    .menu-item, .admin-card {
      background: #f1eded;
      border-radius: 25px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.2);
      overflow: hidden;
      transition: all 0.5s ease;
      position: relative;
    }
    .menu-item:hover, .admin-card:hover {
      transform: translateY(-15px) scale(1.05);
      box-shadow: 0 20px 40px rgba(0,0,0,0.3);
    }
    .menu-item img, .admin-card img {
      width: 100%;
      height: 250px;
      object-fit: cover;
      transition: transform 0.5s ease;
    }
    .menu-item:hover img, .admin-card:hover img {
      transform: scale(1.1);
    }
    .menu-item p, .admin-card h3, .admin-card p {
      padding: 25px;
      margin: 0;
    }
    .admin-card h3 {
      color: #4b0229;
      font-size: 26px;
      font-weight: bold;
    }
    .admin-card p {
      font-style: italic;
      color: #000000;
      font-size: 18px;
    }
    footer {
      background: linear-gradient(135deg, #2c3e50, #34495e);
      color: #ecf0f1;
      text-align: center;
      padding: 30px;
      font-size: 20px;
      box-shadow: 0 -4px 10px rgba(0,0,0,0.2);
    }
  </style>
</head>
<body>
  <header>
    <h1>THE ROYAL BITES</h1>
  </header>
  <nav>
    <a href="#home">Home</a>
    <a href="#menu">Menu</a>
    <a href="#admin">Administration</a>
    <a href="#contact">Contact Us</a>
  </nav>
  <section id="home">
    <h2>Home</h2>
    <h2>Delight in Every Bite</h2>
    <p>The Royal Bite is where tradition meets taste, serving delicious dishes inspired by royal kitchens and timeless flavors.</p>
  </section>
  <section id="menu">
    <h2>Our Menu</h2>
    <div class="menu-grid">
      <div class="menu-item"><img src="panner with naan.png" alt="Grilled Salmon"><p>Naan with Panner Butter Masala</p></div>
      <div class="menu-item"><img src="briyani.png" alt="Vegetable Stir Fry"><p>Chettinad Chicken Briyani</p></div>
      <div class="menu-item"><img src="pepper chicken.png" alt="chicken Burger"><p>Pepper Masala Chicken</p></div>
      <div class="menu-item"><img src="pizza.png" alt="Pasta Primavera"><p>Vegetable Delight Pizza</p></div>
      <div class="menu-item"><img src="lava cake.png" alt="Caesar Salad"><p>Chocolava Cake</p></div>
      <div class="menu-item"><img src="cappucino.png" alt="beversges"><p>Cappucino</p></div>
    </div>
  </section>
  <section id="admin">
    <h2>Administration</h2>
    <div class="admin-grid">
      <div class="admin-card"><img src="chef sanjeev.png" alt="Chef Marco"><h3> Sanjeev</h3><p> Executive chef</p></div>
      <div class="admin-card"><img src="chef rakesh.png" alt="Anna Lee"><h3>Rakesh</h3><p>Head chef</p></div>
    </div>
  </section>
  <section id="contact">
    <h2>Contact Us</h2>
    <p>📍 123 Flavor Street, Downtown City, State 12345</p>
    <p>📞 +1 234 567 8900</p>
    <p>📧 info@theroyalbites.com</p>
  </section>
  <footer>
    Designed by Ashna.M
    25018797
  </footer>
</body>
</html>
```


## OUTPUT:

<img width="1920" height="1021" alt="Screenshot (78)" src="https://github.com/user-attachments/assets/08a77ac4-f4d6-4877-8b1e-d54f83c1d5dd" />

<img width="1920" height="1011" alt="Screenshot (79)" src="https://github.com/user-attachments/assets/ad0e7194-bc23-44a1-8b6c-12f81776a53b" />

<img width="1920" height="1011" alt="Screenshot (80)" src="https://github.com/user-attachments/assets/59a47d0b-865c-47f7-93d6-7873dd1b5280" />

<img width="1920" height="1017" alt="Screenshot (81)" src="https://github.com/user-attachments/assets/686782cf-488d-4d5f-aa32-4c02cdfed102" />

## RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
