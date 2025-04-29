# Ex.07 Restaurant Website
## Date: 29/04/2025
## Name: VISHWA V
## Reg No: 212224110062

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
home.html

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GRAND | Home</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500&family=Playfair+Display:wght@700&family=Montserrat:wght@400&display=swap"
        rel="stylesheet">
    <style>
        /* General Reset & Body */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Roboto', sans-serif;
            color: #333;
            background: linear-gradient(135deg, #f0f4f8, #d9e2ec);
            line-height: 1.6;
            transition: background 0.3s ease;
        }

        /* Header */
        header {
            background: linear-gradient(135deg, #6a11cb, #2575fc);
            color: #ffffff;
            padding: 15px 30px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        header img {
            height: 50px;
            transition: transform 0.3s ease;
        }

        header img:hover {
            transform: scale(1.1);
        }

        nav {
            display: flex;
            gap: 20px;
        }

        nav a {
            text-decoration: none;
            color: white;
            font-weight: 500;
            transition: color 0.3s ease, transform 0.2s ease;
            font-size: 1rem;
        }

        nav a:hover {
            color: #f4b400;
            transform: translateY(-2px);
        }

        /* Banner Section */
        .banner {
            height: 400px;
            background: url('https://source.unsplash.com/1600x900/?restaurant') no-repeat center center/cover;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            position: relative;
            text-shadow: 0 5px 10px rgba(0, 0, 0, 0.7);
        }

        .banner-content {
            background: rgba(0, 0, 0, 0.6);
            padding: 20px 35px;
            border-radius: 10px;
            text-align: center;
            transition: transform 0.3s ease;
        }

        .banner-content h1 {
            font-family: 'Playfair Display', serif;
            font-size: 3rem;
            color: #f4b400;
        }

        .banner-content p {
            margin: 10px 0;
            font-size: 1.2rem;
            color: #e2e8f0;
        }

        .banner-content a {
            text-decoration: none;
            background: #f4b400;
            padding: 10px 20px;
            color: #333;
            font-weight: 700;
            border-radius: 25px;
            transition: background 0.3s ease, transform 0.3s ease;
        }

        .banner-content a:hover {
            background: #e09e00;
            transform: translateY(-3px);
        }

        /* Features Grid Section */
        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            padding: 30px 15px;
            background: #ffffff;
            border-top: 1px solid #d1d5e0;
        }

        .feature {
            background: #f9f9f9;
            padding: 15px;
            border-radius: 15px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            transition: transform 0.2s ease, box-shadow 0.3s ease;
            text-align: center;
        }

        .feature:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
        }

        .feature img {
            max-width: 100%;
            height: 120px;
            object-fit: cover;
            border-radius: 10px;
            transition: transform 0.3s ease;
        }

        .feature img:hover {
            transform: scale(1.1);
        }

        .feature h3 {
            font-family: 'Montserrat', sans-serif;
            margin: 10px 0;
            font-size: 1.1rem;
            color: #333;
        }

        .feature p {
            font-size: 0.9rem;
            color: #555;
        }

        /* Footer */
        footer {
            background: linear-gradient(135deg, #6a11cb, #2575fc);
            color: white;
            text-align: center;
            padding: 15px 20px;
            font-size: 0.9rem;
        }

        footer a {
            color: #f4b400;
            text-decoration: none;
            font-weight: bold;
            transition: color 0.3s ease;
        }

        footer a:hover {
            color: #e09e00;
        }

        /* Responsiveness */
        @media (max-width: 768px) {
            .banner-content h1 {
                font-size: 2.2rem;
            }

            .banner-content p {
                font-size: 1rem;
            }

            header {
                flex-direction: column;
                gap: 10px;
            }
        }

        @media (max-width: 480px) {
            .banner-content h1 {
                font-size: 1.8rem;
            }

            .features {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>

<body>
    <!-- Header Section -->
    <header>
        <img src="logo.webp" alt="Modern Muse Logo">
        <nav>
            <a href="home.html">Home</a>
            <a href="menu.html">Menu</a>
            <a href="contact.html">Contact</a>
            <a href="admin.html">Admin</a>
        </nav>
    </header>

    <!-- Banner Section -->
    <div class="banner">
        <div class="banner-content">
            <h1>GRAND</h1>
            <p>Serving You the Finest Cuisine</p>
            <a href="#features">Discover More</a>
        </div>
    </div>

    <!-- Features Section -->
    <section class="features">
        <div class="feature">
            <img src="dosa.webp" alt="High quality dishes">
            <h3>High Quality Dishes</h3>
            <p>Indulge in the finest and freshest meals crafted with love and expertise.</p>
        </div>
    </section>

    <!-- Footer Section -->
    <footer>
        <p>&copy; 2024 GRAND. All rights reserved. | <a href="#">Privacy Policy</a></p>
    </footer>
</body>

</html>

menu.html

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial initial-scale=1.0">
    <title>GRAND - Menu</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500&family=Playfair+Display:wght@700&display=swap"
        rel="stylesheet">
    <style>
        /* General Reset */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Montserrat', sans-serif;
            background: linear-gradient(to bottom, #e0eafc, #cfdef3);
            line-height: 1.6;
            color: #333;
        }

        /* Header */
        header {
            background: linear-gradient(to right, #4facfe, #00f2fe);
            color: white;
            padding: 15px 30px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        header h1 {
            font-family: 'Playfair Display', serif;
            font-size: 1.8rem;
        }

        header nav a {
            text-decoration: none;
            color: white;
            font-weight: 500;
            margin: 0 15px;
            transition: color 0.3s ease, transform 0.2s ease;
        }

        header nav a:hover {
            color: #ff9800;
            transform: translateY(-2px);
        }

        /* Main Menu Section */
        .menu-container {
            padding: 50px 20px;
            text-align: center;
        }

        .menu-container h1 {
            font-size: 2.7rem;
            color: #333;
            font-family: 'Playfair Display', serif;
            margin-bottom: 20px;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.1);
        }

        .menu-items {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            padding: 20px 10px;
        }

        .menu-item {
            background: white;
            border-radius: 12px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .menu-item img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            transition: transform 0.3s ease;
        }

        .menu-item:hover {
            transform: scale(1.1);
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
        }

        .menu-item:hover img {
            transform: scale(1.15);
        }

        .menu-details {
            padding: 10px 15px;
            text-align: left;
        }

        .menu-details h3 {
            font-size: 1.2rem;
            color: #555;
            font-weight: 600;
            margin-bottom: 5px;
        }

        .menu-details p {
            font-size: 0.9rem;
            color: #666;
        }

        .menu-details .price {
            color: #e74c3c;
            font-weight: bold;
            margin-top: 5px;
        }

        /* Footer */
        footer {
            background: #333;
            color: white;
            text-align: center;
            padding: 15px 0;
            font-size: 0.9rem;
        }

        footer a {
            color: #ff9800;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        footer a:hover {
            color: #f4f4f4;
        }

        /* Media Queries */
        @media (max-width: 768px) {
            header h1 {
                font-size: 1.6rem;
            }

            .menu-items {
                grid-template-columns: 1fr 1fr;
            }
        }

        @media (max-width: 480px) {
            .menu-container h1 {
                font-size: 2rem;
            }

            .menu-items {
                grid-template-columns: 1fr;
            }

            .menu-item img {
                height: 180px;
            }
        }
    </style>
</head>

<body>
    <!-- Header Section -->
    <header>
        <h1>Grand</h1>
        <nav>
            <a href="home.html">Home</a>
            <a href="menu.html">Menu</a>
            <a href="contact.html">Contact</a>
            <a href="admin.html">Admin</a>
        </nav>
    </header>

    <!-- Main Menu Section -->
    <div class="menu-container">
        <h1>Our Menu</h1>
        <div class="menu-items">
            <div class="menu-item">
                <img src="briyani.jpg" alt="Classic Briyani">
                <div class="menu-details">
                    <h3>Classic Briyani</h3>
                    <p class="price">₹599/-</p>
                </div>
            </div>
            <div class="menu-item">
                <img src="chilli.jpg" alt="Chilli Parotta">
                <div class="menu-details">
                    <h3>Chilli Parotta</h3>
                    <p class="price">₹420/-</p>
                </div>
            </div>
            <div class="menu-item">
                <img src="fish.jpg" alt="Fish Prawn">
                <div class="menu-details">
                    <h3>Fish Prawn</h3>
                    <p class="price">₹380/-</p>
                </div>
            </div>
            <div class="menu-item">
                <img src="fishfried.jpg" alt="Fish Fried">
                <div class="menu-details">
                    <h3>Fish Fried</h3>
                    <p class="price">₹400/-</p>
                </div>
            </div>
            <div class="menu-item">
                <img src="rice.jpg" alt="Fried rice">
                <div class="menu-details">
                    <h3>Fried rice</h3>
                    <p class="price">₹320/-</p>
                </div>
            </div>
            <div class="menu-item">
                <img src="rosemilk.jpg" alt="rosemilk">
                <div class="menu-details">
                    <h3>rosemilk</h3>
                    <p class="price">₹300/-</p>
                </div>
            </div>
            <div class="menu-item">
                <img src="wine.jpg" alt="Wine">
                <div class="menu-details">
                    <h3>wine</h3>
                    <p class="price">₹700/-</p>
                </div>
            </div>

        </div>
    </div>

    <!-- Footer Section -->
    <footer>
        <p>&copy; 2024 GRAND | <a href="#">Back to Home</a></p>
    </footer>
</body>

</html>

contact.html

<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Grand - Contact Us</title>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500&family=Playfair+Display:wght@700&display=swap"
    rel="stylesheet">
  <style>
    /* General Reset */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Montserrat', sans-serif;
      line-height: 1.6;
      background: linear-gradient(to bottom, #eef2f3, #8ec5fc);
      color: #333;
    }

    /* Header Section */
    header {
      background: linear-gradient(to right, #6a11cb, #2575fc);
      color: white;
      padding: 15px 30px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
      position: sticky;
      top: 0;
      z-index: 100;
    }

    header img {
      height: 50px;
      border-radius: 5px;
    }

    header nav a {
      text-decoration: none;
      color: white;
      font-weight: 500;
      margin: 0 15px;
      transition: color 0.3s ease, transform 0.2s ease;
      font-size: 1rem;
    }

    header nav a:hover {
      color: #ff9800;
      transform: translateY(-2px);
    }

    /* Contact Banner Section */
    .contact-banner {
      display: flex;
      align-items: center;
      justify-content: center;
      background: url('https://source.unsplash.com/1600x600/?city,contact') no-repeat center center/cover;
      color: white;
      height: 400px;
      text-shadow: 0 4px 8px rgba(0, 0, 0, 0.7);
      text-align: center;
    }

    .contact-banner h1 {
      font-family: 'Playfair Display', serif;
      font-size: 3rem;
      color: #ffd700;
    }

    /* Contact Section - Form and Details */
    .contact-section {
      display: flex;
      justify-content: space-between;
      padding: 50px 20px;
      gap: 30px;
      flex-wrap: wrap;
    }

    .contact-details,
    .contact-form {
      background: white;
      padding: 20px 30px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      flex: 1 1 400px;
      max-width: 500px;
    }

    /* Contact Info Styling */
    .contact-details h2 {
      font-size: 1.8rem;
      margin-bottom: 15px;
      color: #333;
      font-family: 'Playfair Display', serif;
      text-align: center;
    }

    .contact-details p {
      margin: 10px 0;
      font-size: 1rem;
      color: #555;
    }

    /* Contact Form */
    .contact-form h2 {
      font-size: 1.8rem;
      color: #333;
      font-family: 'Playfair Display', serif;
      text-align: center;
      margin-bottom: 10px;
    }

    .contact-form input,
    .contact-form textarea {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 5px;
      font-size: 1rem;
    }

    .contact-form textarea {
      height: 120px;
    }

    .contact-form button {
      background: #ff9800;
      color: white;
      border: none;
      padding: 12px 20px;
      width: 100%;
      font-size: 1.1rem;
      cursor: pointer;
      border-radius: 5px;
      transition: background 0.3s ease;
    }

    .contact-form button:hover {
      background: #e67e22;
    }

    /* Footer Section */
    footer {
      background: #333;
      color: white;
      text-align: center;
      padding: 15px 0;
      font-size: 0.9rem;
    }

    footer a {
      color: #ff9800;
      text-decoration: none;
      transition: color 0.3s ease;
    }

    footer a:hover {
      color: #fff;
    }

    /* Media Queries */
    @media (max-width: 768px) {
      .contact-section {
        flex-direction: column;
        align-items: center;
      }

      header nav a {
        font-size: 0.9rem;
      }

      .contact-form,
      .contact-details {
        max-width: 100%;
      }
    }

    @media (max-width: 480px) {
      .contact-banner h1 {
        font-size: 2.5rem;
      }
    }
  </style>
</head>

<body>
  <!-- Header Section -->
  <header>
    <img src="https://via.placeholder.com/50" alt="Logo">
    <nav>
      <a href="home.html">Home</a>
      <a href="menu.html">Menu</a>
      <a href="contact.html">Contact</a>
      <a href="admin.html">Admin</a>
    </nav>
  </header>

  <!-- Contact Banner Section -->
  <div class="contact-banner">
    <h1>Contact Us</h1>
  </div>

  <!-- Contact Section -->
  <section class="contact-section">
    <div class="contact-details">
      <h2>Our Address</h2>
      <p><strong>Address:</strong> Grand, Chennai, Tamil Nadu, India</p>
      <p><strong>Phone:</strong> +91 9342561326</p>
      <p><strong>Email:</strong> Grand@gmail.com</p>
      <p><strong>Hours:</strong> Mon - Sun: 24/7</p>
    </div>
    <div class="contact-form">
      <h2>Get in Touch</h2>
      <input type="text" placeholder="Your Name">
      <input type="email" placeholder="Your Email">
      <textarea placeholder="Your Message"></textarea>
      <button type="submit">Send Message</button>
    </div>
  </section>
  <footer>
    designed by,VISHWA V[212224110062]
  </footer>
</body>
```
## OUTPUT:

![Screenshot 2025-04-29 141114](https://github.com/user-attachments/assets/076bdd3c-f74f-4b76-b35e-5437e3862401)

![Screenshot 2025-04-29 141139 - Copy](https://github.com/user-attachments/assets/6d35ec04-6f61-4030-8109-8d532c1566b0)

![Screenshot 2025-04-29 141303](https://github.com/user-attachments/assets/67617f65-8d7d-4e40-942d-53a288594ffb)

## RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
