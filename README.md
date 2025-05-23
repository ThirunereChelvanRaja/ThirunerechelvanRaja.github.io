<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Thirunere Chelvan Raja - Portfolio</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Roboto', sans-serif;
      color: #fff;
      background: linear-gradient(to right, #0f2027, #203a43, #2c5364);
    }

    nav {
      background-color: rgba(0,0,0,0.8);
      padding: 1rem;
      text-align: center;
      position: sticky;
      top: 0;
      z-index: 999;
    }

    nav ul {
      list-style: none;
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
    }

    nav ul li {
      margin: 0 15px;
    }

    nav ul li a {
      color: #00f7ff;
      text-decoration: none;
      font-weight: bold;
      transition: 0.3s;
    }

    nav ul li a:hover {
      color: #ffdd57;
    }

    section {
      padding: 80px 20px;
      max-width: 1200px;
      margin: auto;
      opacity: 0;
      transform: translateY(40px);
      transition: all 1s ease-out;
    }

    section.show {
      opacity: 1;
      transform: translateY(0);
    }

    .banner {
      background-image: url('BACKGROUND.png');
      background-size: cover;
      background-position: center;
      color: #fff;
      text-align: center;
      padding: 140px 20px 160px;
    }

    .banner h1 {
      font-size: 3rem;
      animation: slideIn 1s ease forwards;
    }

    .banner p {
      font-size: 1.5rem;
      margin-top: 10px;
      animation: fadeIn 1.5s ease forwards;
    }

    .buttons {
      margin-top: 30px;
      animation: fadeIn 2s ease forwards;
    }

    .buttons a {
      display: inline-block;
      margin: 0 10px;
      background: #00f7ff;
      padding: 10px 20px;
      color: #000;
      text-decoration: none;
      border-radius: 30px;
      transition: background 0.3s ease;
    }

    .buttons a:hover {
      background: #ffdd57;
      color: #000;
    }

    h2 {
      font-size: 2rem;
      margin-bottom: 20px;
      text-align: center;
      color: #00f7ff;
    }

    .skills ul, .services ul {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
      gap: 10px;
      list-style: none;
      padding: 0;
      text-align: center;
    }

    .skills li, .services li {
      background: rgba(255,255,255,0.1);
      padding: 15px;
      border-radius: 10px;
      transition: transform 0.3s;
    }

    .skills li:hover, .services li:hover {
      transform: scale(1.05);
    }

    .project {
      background: rgba(255,255,255,0.1);
      padding: 20px;
      margin: 10px 0;
      border-radius: 10px;
    }

    .footer {
      text-align: center;
      padding: 30px;
      background: rgba(0,0,0,0.8);
      color: #aaa;
      margin-top: 50px;
    }

    @keyframes slideIn {
      from {
        transform: translateY(-50px);
        opacity: 0;
      }
      to {
        transform: translateY(0);
        opacity: 1;
      }
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    .about-img {
      border-radius: 50%;
      width: 200px;
      height: 200px;
      object-fit: cover;
      border: 4px solid #00f7ff;
    }

    .about-content {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      gap: 30px;
    }

    .about-text {
      flex: 2;
      min-width: 300px;
    }

    .about-list {
      list-style: none;
      padding: 0;
      line-height: 1.8;
    }

    .about-list i {
      margin-right: 10px;
    }

    .about-img-wrapper {
      flex: 1;
      min-width: 250px;
      text-align: center;
    }

    .about-quote {
      text-align: center;
      margin-top: 30px;
      font-style: italic;
      color: #ccc;
    }

    /* Certificates */
    #certificates .cert-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
      padding: 20px 0;
    }

    #certificates .cert {
      background: rgba(255,255,255,0.1);
      padding: 20px;
      border-radius: 10px;
      transition: transform 0.3s ease;
      text-align: center;
    }

    #certificates .cert h3 {
      color: #00f7ff;
      margin-bottom: 10px;
    }

    #certificates .cert a {
      display: inline-block;
      margin-top: 10px;
      background: #00f7ff;
      padding: 8px 16px;
      color: #000;
      text-decoration: none;
      border-radius: 30px;
      transition: background 0.3s;
    }

    #certificates .cert a:hover {
      background: #ffdd57;
      color: #000;
    }

    #certificates .cert:hover {
      transform: scale(1.05);
    }
  </style>
  <script>
    window.addEventListener('scroll', () => {
      document.querySelectorAll('section').forEach(sec => {
        const top = window.scrollY;
        const offset = sec.offsetTop - 400;
        const height = sec.offsetHeight;
        if (top >= offset && top < offset + height) {
          sec.classList.add('show');
        }
      });
    });
  </script>
</head>
<body>
  <header>
    <nav>
      <ul>
        <li><a href="#banner">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#certificates">Certificates</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#services">Services</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <section class="banner" id="banner">
    <h1>Thirunere Chelvan Raja</h1>
    <p>Data Analyst / Senior Software Engineer</p>
    <div class="buttons">
      <a href="https://www.linkedin.com/in/thirunere-chelvan-r-432a3b269/" target="_blank">LinkedIn</a>
      <a href="https://1drv.ms/b/c/c7596397057207b8/EYtCRlwkXUtItixJE0ZDjmsBR-b5EF_0y2V81a9MZWUuYA" download>Download Resume</a>
    </div>
  </section>

  <section id="about">
    <h2>About Me</h2>
    <div class="about-content">
      <div class="about-img-wrapper">
        <img src="C:\Users\Thirunere Chelvan R\thiru-portfolio\my_image.jpeg" alt="Thirunere Chelvan Raja" class="about-img" />
      </div>
      <div class="about-text">
        <ul class="about-list">
          <li><i class="fas fa-briefcase" style="color: #ffdd57;"></i> 3+ years of experience in data analytics and software engineering.</li>
          <li><i class="fas fa-tools" style="color: #00f7ff;"></i> Skilled in SQL, Python (Pandas, NumPy), Tableau, Power BI, Excel.</li>
          <li><i class="fas fa-lightbulb" style="color: #ffdd57;"></i> Combines technical expertise with a business-first mindset.</li>
          <li><i class="fas fa-chart-line" style="color: #00f7ff;"></i> Builds dashboards, automates reports, and delivers EDA insights.</li>
          <li><i class="fas fa-brain" style="color: #ffdd57;"></i> Passionate about solving problems with data-driven strategies.</li>
        </ul>
      </div>
    </div>
    <p class="about-quote">"Turning data into decisions is not just a job — it's a mindset."</p>
  </section>

  <section id="skills" class="skills">
    <h2>Skills</h2>
    <ul>
      <li>Python</li>
      <li>SQL</li>
      <li>Pandas</li>
      <li>Power BI</li>
      <li>Tableau</li>
      <li>Excel</li>
      <li>Data Cleaning</li>
      <li>EDA</li>
      <li>Dashboards</li>
    </ul>
  </section>

  <section id="certificates">
    <h2>Certificates</h2>
    <div class="cert-grid">
      <div class="cert">
        <h3>Python</h3>
        <p>Data analysis and scripting using Python.</p>
      </div>
      <div class="cert">
        <h3>Data Visualization using Python</h3>
        <p>Charts, plots, and dashboards with Matplotlib and Seaborn.</p>
      </div>
      <div class="cert">
        <h3>Advanced Excel</h3>
        <p>Data modeling, pivot tables, formulas, and VBA.</p>
      </div>
      <div class="cert">
        <h3>Machine Learning</h3>
        <p>Supervised/Unsupervised learning models and evaluation.</p>
      </div>
      <div class="cert">
        <h3>R Programming</h3>
        <p>Statistical computing and data visualization using R.</p>
      </div>
      <div class="cert">
        <h3>Project Management</h3>
        <p>Agile, Scrum, Kanban methodologies and tools.</p>
      </div>
      <div class="cert">
        <h3>GenAI</h3>
        <p>Understanding generative AI and prompt engineering basics.</p>
      </div>
      <div class="cert">
        <h3>AI Tools for All</h3>
        <p>Exploration of top AI tools for productivity and automation.</p>
      </div>
    </div>
  </section>

  <section id="projects">
    <h2>Projects</h2>
    <div class="project">
      <h3>Customer Purchase Behavior Analysis</h3>
      <p>Analyzed transactional data to identify purchasing patterns and customer segmentation using Python and Power BI.</p>
    </div>
    <div class="project">
      <h3>Sales Forecasting Model</h3>
      <p>Built time-series forecasting models to predict monthly sales trends and provided reports using Tableau dashboards.</p>
    </div>
  </section>

  <section id="services" class="services">
    <h2>Services</h2>
    <ul>
      <li>Data Cleaning</li>
      <li>Dashboarding</li>
      <li>Exploratory Data Analysis</li>
      <li>Reporting & BI</li>
      <li>Predictive Modeling</li>
    </ul>
  </section>

  <section id="contact">
    <h2>Contact</h2>
    <p>Email: rthirunerechelvan@gmail.com</p>
    <p>Phone: +91 74834 48762</p>
    <p>Location: Bengaluru, Karnataka, India</p>
  </section>

  <footer class="footer">
    <p>&copy; 2025 Thirunere Chelvan Raja. All Rights Reserved.</p>
  </footer>
</body>
</html>
