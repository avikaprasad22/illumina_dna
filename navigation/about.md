---
layout: tailwind
# title: About Us
permalink: /about/
show_reading_time: false 
menu: nav/home.html
---
<style>
  body {
    font-family: Arial, sans-serif;
    text-align: center;
  }
  
  .header {
    background: linear-gradient(to bottom, #cce4ff, white);
    padding: 20px 6px;
    color: black;
  }

  .header h1 {
    font-size: 40px;
    font-weight: bold;
    color: #1e3a8a;
  }

  .content {
    max-width: 800px;
    margin: 0 auto;
    font-size: 18px;
    color: #4b5563;
  }

  .section {
    max-width: 900px;
    margin: 40px auto;
    padding: 16px;
  }

  .section h2 {
    font-size: 30px;
    font-weight: bold;
    color: #1e3a8a;
  }

  .buttons button {
    background-color: #2563eb;
    color: white;
    padding: 12px 24px;
    border: none;
    border-radius: 25px;
    font-size: 18px;
    font-weight: bold;
    cursor: pointer;
    margin: 10px;
    box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.2);
  }

  .buttons button:hover {
    background-color: #1d4ed8;
  }

  .popup {
    position: fixed;
    inset: 0;
    background: rgba(0, 0, 0, 0.6);
    display: none;
    align-items: center;
    justify-content: center;
  }

  .popup-content {
    background: white;
    color: black; 
    padding: 20px;
    border-radius: 10px;
    width: 350px;
    position: relative;
    box-shadow: 2px 2px 20px rgba(0, 0, 0, 0.3);
  }

  .popup-content button {
    position: absolute;
    top: 10px;
    right: 10px;
    font-size: 20px;
    background: none;
    border: none;
    cursor: pointer;
  }

  .popup ul {
    text-align: left;
    color: #4b5563;
  }
</style>

<div class="header">
  <h1>🚀 About Us</h1>
  <p class="content">
    The Illumina Biotech Education Game is an innovative initiative designed to engage students and the community in the fascinating world of biotechnology. Through interactive gameplay and real-world challenges, participants explore DNA, genetics, and cutting-edge scientific advancements in a fun and immersive way.
  </p>
</div>

<div class="section">
  <h2>🌍 Our Mission & Vision</h2>
  <p class="content">
    Our mission is to inspire the next generation of scientists and innovators by making biotechnology accessible and engaging. We envision a world where learning is interactive, inclusive, and drives curiosity in STEM fields.
  </p>
</div>

<div class="buttons">
  <button onclick="openPopup('teamPopup')">Meet Our Team</button>
  <button onclick="openPopup('historyPopup')">Our Journey</button>
  <button onclick="openPopup('contactPopup')">Contact Us</button>
</div>

<div id="teamPopup" class="popup" onclick="closePopup(event, 'teamPopup')">
  <div class="popup-content">
    <button onclick="closePopup(event, 'teamPopup')">&times;</button>
    <h2>👨‍💻 Our Team</h2>
    <ul>
      <li><strong>Avika</strong> - Scrum Master</li>
      <li><strong>Nora</strong> - Assistant Scrum Master</li>
      <li><strong>Soni</strong> - DNA Sequencing Simulation</li>
      <li><strong>Katherine</strong> - UI Design and Implementation</li>
      <li><strong>Gabi</strong> - Trivia Question System</li>
      <li><strong>Zoe</strong> - Trivia Question System</li>
    </ul>
  </div>
</div>

<div id="historyPopup" class="popup" onclick="closePopup(event, 'historyPopup')">
  <div class="popup-content">
    <button onclick="closePopup(event, 'historyPopup')">&times;</button>
    <h2>📜 Our History</h2>
    <ul>
      <li><strong>March 2025</strong> - Conceptualized the biotech education platform</li>
      <li><strong>April 2025</strong> - Launched first interactive game prototype</li>
      <li><strong>May 2025</strong> - xx</li>
    </ul>
  </div>
</div>

<div id="contactPopup" class="popup" onclick="closePopup(event, 'contactPopup')">
  <div class="popup-content">
    <button onclick="closePopup(event, 'contactPopup')">&times;</button>
    <h2>📩 Get in Touch</h2>
    <p>Email: <a href="mailto:contact@yourcompany.com">katherine.yx.chen@gmail.com</a></p>
    <p>Phone: +1 (858) 456-7890</p>
    <p>We are excited to collaborate with you!</p>
  </div>
</div>

<script>
  function openPopup(id) {
    document.getElementById(id).style.display = "flex";
  }

  function closePopup(event, id) {
    if (event.target.classList.contains("popup") || event.target.tagName === "BUTTON") {
      document.getElementById(id).style.display = "none";
    }
  }

  document.addEventListener("keydown", function (event) {
    if (event.key === "Escape") {
      document.querySelectorAll(".popup").forEach(popup => popup.style.display = "none");
    }
  });
</script>
