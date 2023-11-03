<!DOCTYPE html>
<html>
  <head>
    <title>Project Management Tool</title>
  </head>
  <style>
    body,
    h1,
    h2,
    p {
      margin: 0;
      padding: 0;
    }

    body {
      font-family: Arial, sans-serif;
      background-color: #f0f0f0;
      color: #333;
      line-height: 1.6;
      margin: 0;
      padding: 0;
      background-image:url('pms.png');
      background-size: cover;
      background-attachment:fixed;
    }

    header {
      background-color: #007acc;
      color: #fff;
      padding: 20px;
      text-align: center;
    }

    section {
      background-color: #fff;
      margin: 93px;
      padding: 20px;
      border: 1px solid #ccc;
    }

    input[type="text"],
    input[type="password"],
    button {
      display: block;
      width: 100%;
      margin-bottom: 10px;
      padding: 10px;
    }

    section#social-media,
    section#task-assignment {
      border-radius: 10px;
      opacity:0.9;
      
    }

    footer {
      background-color: #007acc;
      color: #fff;
      text-align: center;
      padding: 10px;
    }

    a {
      color: #007acc;
      text-decoration: none;
      transition: color 0.3s;
    }

    a:hover {
      color: #00588d;
    }

    button {
      background-color: #007acc;
      color: #fff;
      border: none;
      padding: 10px 20px;
      cursor: pointer;
    }

    button:hover {
      background-color: #00588d;
    }
  </style>
  <body>
    <header>
      <h1>Welcome to Your Project Management Tool</h1>
    </header>

    <section id="social-media">
      <a href="/media.html"><h2>Social Media Feed</h2></a>
    </section>

    <section id="task-assignment">
      <a href="/task.html"><h2>Task Assignment</h2></a>
    </section>

    <footer>
      <p>&copy; 2023 Project Management Tool</p>
    </footer>

    <script>
      document.addEventListener("DOMContentLoaded", function () {
        function showSection(sectionId) {
          const sections = document.querySelectorAll("section");
          sections.forEach((section) => {
            section.style.display = "none";
          });
          document.getElementById(sectionId).style.display = "block";
        }

        const links = document.querySelectorAll("nav a");
        links.forEach((link) => {
          link.addEventListener("click", function (event) {
            event.preventDefault();
            showSection(link.getAttribute("data-section"));
          });
        });
      });
    </script>
  </body>
</html>
