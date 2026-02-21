<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Professional Navigation Menu</title>

<style>
/* ===== Reset ===== */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  scroll-behavior: smooth;
}

/* ===== Page Background ===== */
body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  line-height: 1.6;
  color: #e5e7eb;
  background: linear-gradient(135deg, #0f172a, #1e293b);
}

/* ===== Color System ===== */
:root{
  --nav-bg: rgba(15, 23, 42, 0.7);
  --text: #e5e7eb;
  --primary: #38bdf8;       /* cyan */
  --primary-dark: #0ea5e9;
}

/* ===== Navbar ===== */
nav {
  position: fixed;
  top: 0;
  width: 100%;
  display: flex;
  justify-content: center;
  gap: 30px;
  padding: 15px 20px;
  background: var(--nav-bg);
  backdrop-filter: blur(10px);
  transition: all 0.3s ease;
  z-index: 1000;
}

/* Shadow on scroll */
nav.scrolled {
  box-shadow: 0 4px 15px rgba(0,0,0,0.4);
}

/* ===== Links ===== */
nav a {
  position: relative;
  color: var(--text);
  text-decoration: none;
  font-weight: 500;
  padding: 8px 12px;
  transition: color 0.3s ease, transform 0.2s ease;
}

/* Underline */
nav a::after {
  content: "";
  position: absolute;
  left: 0;
  bottom: -4px;
  width: 0%;
  height: 2px;
  background-color: var(--primary);
  transition: width 0.3s ease;
}

/* Hover */
nav a:hover {
  color: var(--primary);
  transform: translateY(-2px);
}

nav a:hover::after {
  width: 100%;
}

/* Active */
nav a.active {
  color: var(--primary-dark);
}

nav a.active::after {
  width: 100%;
  background-color: var(--primary-dark);
}

/* ===== Sections ===== */
section {
  padding: 120px 20px;
  min-height: 100vh;
  border-bottom: 1px solid rgba(255,255,255,0.1);
}

h1 {
  font-size: 2.5rem;
  margin-bottom: 20px;
  color: white;
}

p {
  max-width: 700px;
  font-size: 1.1rem;
  color: #cbd5e1;
}
</style>
</head>

<body>

<!-- ===== Navigation ===== -->
<nav id="navbar">
  <a href="#home" class="nav-link active">Home</a>
  <a href="#about" class="nav-link">About</a>
  <a href="#services" class="nav-link">Services</a>
  <a href="#contact" class="nav-link">Contact</a>
</nav>

<!-- ===== Sections ===== -->
<section id="home">
  <h1>Home</h1>
  <p>Welcome to our professional page. Scroll to explore different sections and see how the navigation bar responds.</p>
</section>

<section id="about">
  <h1>About</h1>
  <p>This section gives information about us. The navbar stays visible and interactive as you scroll.</p>
</section>

<section id="services">
  <h1>Services</h1>
  <p>We offer high-quality beginner-friendly web development services. Every project helps you grow!</p>
</section>

<section id="contact">
  <h1>Contact</h1>
  <p>Get in touch through email or phone. We’d love to hear from you and discuss future opportunities.</p>
</section>

<!-- ===== JavaScript ===== -->
<script>
const navbar = document.getElementById('navbar');
const navLinks = document.querySelectorAll('.nav-link');

window.addEventListener('scroll', () => {

  if (window.scrollY > 50) {
    navbar.classList.add('scrolled');
  } else {
    navbar.classList.remove('scrolled');
  }

  let current = '';
  document.querySelectorAll("section").forEach(section => {
    const sectionTop = section.offsetTop - 120;
    if (window.scrollY >= sectionTop) {
      current = section.getAttribute("id");
    }
  });

  navLinks.forEach(link => {
    link.classList.remove("active");
    if (link.getAttribute("href") === "#" + current) {
      link.classList.add("active");
    }
  });
});
</script>

</body>
</html>
