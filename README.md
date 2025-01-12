# PRODIGY_WD_01
This respository is a responsive and interactive webpage featuring a fixed-position navigation menu that changes its style dynamically when the user scrolls down or hovers over the menu items. The website includes multiple content sections such as "Home," "About Us," "Services," and "Contact Us," each with smooth animations and transitions.
CODE
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Interactive Navigation Menu</title>
  <style>
    
    body, html {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: #f4f4f9;
      color: #333;
    }

    h1, h2 {
      text-align: center;
      color: #333;
    }

    .navbar {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      background-color: #333;
      z-index: 1000;
      transition: background-color 0.3s ease, box-shadow 0.3s ease;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    }

    .navbar ul {
      margin: 0;
      padding: 0;
      list-style: none;
      display: flex;
      justify-content: center;
    }

    .navbar li {
      padding: 20px 30px;
      transition: transform 0.2s ease;
    }

    .navbar a {
      color: white;
      text-decoration: none;
      font-size: 18px;
      text-transform: uppercase;
      transition: color 0.3s ease, transform 0.3s ease;
    }

    .navbar a:hover {
      color: #ff6347;
      transform: scale(1.1);
    }

    .scrolled {
      background-color: #222;
      box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2);
    }

    .content {
      margin-top: 80px;
      padding: 50px 20px;
    }

    .section {
      margin-bottom: 60px;
      padding: 40px 20px;
      background-color: #fff;
      border-radius: 8px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s ease;
    }

    .section:hover {
      transform: scale(1.02);
    }

    .section h2 {
      margin-bottom: 20px;
      font-size: 28px;
      color: #333;
    }

    .section p {
      font-size: 16px;
      line-height: 1.6;
      color: #666;
    }

    .cta-button {
      display: block;
      width: 200px;
      margin: 30px auto 0;
      padding: 15px 0;
      background-color: #ff6347;
      color: white;
      text-align: center;
      text-decoration: none;
      font-size: 18px;
      border-radius: 5px;
      transition: background-color 0.3s ease;
    }

    .cta-button:hover {
      background-color: #e53e35;
    }

    .footer {
      text-align: center;
      padding: 20px;
      background-color: #333;
      color: white;
      position: relative;
      bottom: 0;
      width: 100%;
    }

    .fade-in {
      opacity: 0;
      animation: fadeIn 1.5s forwards;
    }

    @keyframes fadeIn {
      100% {
        opacity: 1;
      }
    }

    @media (max-width: 768px) {
      .navbar ul {
        flex-direction: column;
      }

      .navbar li {
        padding: 15px;
      }
    }
  </style>
</head>
<body>

  <div class="navbar" id="navbar">
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </div>

  <div class="content">
    <section class="section fade-in" id="home">
      <h2>Welcome to Our Website</h2>
      <p>We offer innovative solutions to help you grow your business. Explore our services, learn more about our mission, and get in touch with us today!</p>
      <a href="#about" class="cta-button">Learn More</a>
    </section>

    <section class="section fade-in" id="about">
      <h2>About Us</h2>
      <p>We are a team of passionate individuals committed to providing high-quality digital solutions. Our expertise spans web development, digital marketing, and design. We believe in delivering exceptional results for every project we undertake.</p>
    </section>

    <section class="section fade-in" id="services">
      <h2>Our Services</h2>
      <p>We offer a wide range of services designed to meet your needs:</p>
      <ul>
        <li> Web Development</li>
        <li> Design Thinking</li>
        <li> Digital Marketing</li>
        <li> E-commerce Solutions</li>
      </ul>
      <a href="#contact" class="cta-button">Get Started</a>
    </section>

    <section class="section fade-in" id="contact">
      <h2>Contact Us</h2>
      <p>If you are ready to take your business to the next level, get in touch with us! We're here to help.</p>
      <a href="mailto:contact@yourwebsite.com" class="cta-button">Send an Email</a>
    </section>
  </div>

  <div class="footer">
    <p>&copy; 2025 Your Website. All Rights Reserved.</p>
  </div>

  <script>

    window.onscroll = function() {
      var navbar = document.getElementById("navbar");
      if (window.scrollY > 50) {
        navbar.classList.add("scrolled");
      } else {
        navbar.classList.remove("scrolled");
      }
    };

    window.onload = function() {
      const sections = document.querySelectorAll('.fade-in');
      sections.forEach(section => {
        section.classList.add('fade-in');
      });
    };
  </script>

</body>
</html>
