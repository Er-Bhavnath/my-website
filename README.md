<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>My Portfolio</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      scroll-behavior: smooth;
      box-sizing: border-box;
    }

    body {
      font-family: Arial, sans-serif;
    }

    header {
    
      
        background-color: rgba(51, 51, 51, 0.9);
  color: white;
  padding: 15px;
  position: fixed;
  top: 0;
  width: 100%;
  z-index: 1000;
  transition: top 0.2s ease;





    }

    nav {
      display: flex;
      justify-content: center;
    }

    nav a {
      color: white;
      text-decoration: none;
      margin: 0 15px;
      font-weight: bold;
      padding: 8px 15px;
    }

    nav a:hover {
      background-color: #00adb5;
      border-radius: 5px;
    }

    section {
      padding: 100px 30px;
      min-height: 100vh;
    }

    #home { background-color: #e3f2fd; }
    #about { background-color: #f1f8e9; }
    #projects { background-color: #fff8e1; }
    #skills { background-color: #ede7f6; }
    #certifications { background-color: #fce4ec; }
    #contact { background-color: #f0f4c3; }

    h1 {
      font-size: 3rem;
      margin-bottom: 10px;
      text-align: center;


    }

    p {
      font-size: 1rem;
      line-height: 1.6;
    }

    .center-bold-big {
      text-align: center;
      font-weight: bold;
      font-size: 32px; /* You can adjust the size */
      color: #00adb5;
    }



  </style>
</head>
<body>

  <header id="main-header">

      <div class= center-bold-big href="#home"> Bhavnath Jha </div>

    <nav>
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#projects">Projects</a>
      <a href="#skills">Skills</a>
      <a href="#certifications">Certifications</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <section id="home">
    <h1>Home</h1>
    <p>Welcome to my portfolio!</p>
  </section>

  <section id="about">
    <h1>About</h1>
    <p>I am a passionate IT graduate currently pursuing my Master's in Information Technology from BSBI Berlin. I love coding and learning new technologies.</p>
  </section>

  <section id="projects">
    <h1>Projects</h1>
    <p>• Carbon Footprint Calculator using Python<br>• Berlin Tourist Website using HTML/CSS</p>
  </section>

  <section id="skills">
    <h1>Skills</h1>
    <p>Python, IT Support, HTML, CSS, Communication, Troubleshooting</p>
  </section>

  <section id="certifications">
    <h1>Certifications</h1>
    <p>• Python – Scaler Academy<br>• DSA – Board Infinity</p>
  </section>

  <section id="contact">
    <h1>Contact</h1>
    <p>Email: your.email@example.com<br>LinkedIn: linkedin.com/in/your-profile</p>
  </section>



<script>
  const header = document.getElementById('main-header');
  const body = document.body;
  let lastScroll = window.scrollY;
  let headerVisible = true;

  function showHeader() {
    if (!headerVisible) {
      header.style.top = "0";
      body.style.paddingTop = header.offsetHeight + "px";
      headerVisible = true;
    }
  }

  function hideHeader() {
    if (headerVisible) {
      header.style.top = "-" + header.offsetHeight + "px";
      body.style.paddingTop = "0";
      headerVisible = false;
    }
  }

  window.addEventListener('scroll', () => {
    const currentScroll = window.scrollY;

    if (currentScroll > lastScroll) {
      hideHeader(); // scrolling down
    } else {
      showHeader(); // scrolling up
    }

    lastScroll = currentScroll;
  });

  document.addEventListener('mousemove', (e) => {
    if (e.clientY < 50) {
      showHeader(); // show if the mouse moves near the top
    }
  });

  // Initial setup
  body.style.paddingTop = header.offsetHeight + "px";

</script>


</body>




</html>
