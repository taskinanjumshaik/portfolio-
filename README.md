# portfolio-
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>My Portfolio</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f5f5f5;
    }
    header {
      background-color: #222;
      color: white;
      padding: 15px 0;
      text-align: center;
    }
    nav a {
      color: white;
      margin: 0 15px;
      text-decoration: none;
      font-weight: bold;
      transition: 0.3s;
    }
    nav a:hover {
      color: #00c3ff;
    }
    section {
      padding: 40px;
      text-align: center;
    }

    /* Section Colors */
    #home {
      background-color: #ffffff;
    }
    #portfolio {
      background-color: #e6f2ff;
    }
    #gallery {
      background-color: #f0f0f0;
    }
    #contact {
      background-color: #e6ffe6;
    }

    .card {
      display: inline-block;
      width: 200px;
      margin: 15px;
      padding: 20px;
      background: white;
      border-radius: 10px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.2);
      transition: transform 0.3s, box-shadow 0.3s;
    }
    .card:hover {
      transform: translateY(-10px);
      box-shadow: 0 4px 15px rgba(0,0,0,0.3);
    }

    .rect-image {
      width: 80%;
      max-width: 600px;
      height: auto;
      border-radius: 15px;
      margin: 20px auto;
      display: block;
      box-shadow: 0 4px 10px rgba(0,0,0,0.2);
    }

    .gallery img {
      width: 250px;
      height: 150px;
      margin: 10px;
      object-fit: cover;
      border-radius: 15px;
      transition: transform 0.3s;
      box-shadow: 0 2px 8px rgba(0,0,0,0.2);
    }
    .gallery img:hover {
      transform: scale(1.1);
    }

    input, textarea {
      padding: 10px;
      margin: 10px;
      width: 80%;
      max-width: 400px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    button {
      padding: 10px 20px;
      background: #007acc;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    button:hover {
      background: #005e99;
    }
  </style>
</head>
<body>

  <header>
    <h1>My Portfolio</h1>
    <nav>
      <a href="#home">Home</a>
      <a href="#portfolio">Portfolio</a>
      <a href="#gallery">Gallery</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <section id="home">
    <h2>Welcome!</h2>
    <p>This is my personal portfolio website.</p>
    <img src="https://via.placeholder.com/800x300?text=Welcome+Image" alt="Banner" class="rect-image">
  </section>

  <section id="portfolio">
    <h2>Projects</h2>
    <div class="card">Transport Management System</div>
    <div class="card">Weather App</div>
    <div class="card">Portfolio Website</div>
  </section>

  <section id="gallery">
    <h2>Gallery</h2>
    <div class="gallery">
      <img src="https://source.unsplash.com/random/400x300?tech" alt="Gallery 1" />
      <img src="https://source.unsplash.com/random/400x300?code" alt="Gallery 2" />
      <img src="https://source.unsplash.com/random/400x300?laptop" alt="Gallery 3" />
    </div>
  </section>

  <section id="contact">
    <h2>Contact Me</h2>
    <input type="text" id="name" placeholder="Your Name" /><br/>
    <input type="email" id="email" placeholder="Your Email" /><br/>
    <textarea id="message" rows="4" placeholder="Your Message"></textarea><br/>
    <button onclick="submitForm()">Send</button>
    <p id="response" style="color: green; margin-top: 10px;"></p>
  </section>

  <script>
    function submitForm() {
      const name = document.getElementById('name').value.trim();
      const email = document.getElementById('email').value.trim();
      const message = document.getElementById('message').value.trim();

      if (name && email && message) {
        document.getElementById('response').innerText = "Thanks for contacting me!";
      } else {
        document.getElementById('response').innerText = "Please fill out all fields.";
      }
    }
  </script>

</body>
</html>
