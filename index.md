---
layout: posts
author_profile: false
---

<style>
  /* הגדרת הרקע הקבוע - Parallax */
  body {
    margin: 0;
    padding: 0;
  }
  
  .hero-section {
    position: relative;
    height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    color: white;
    /* החלף את הלינק למטה בתמונת הרקע הנקייה שתרצה */
    background-image: url('https://images.unsplash.com/photo-1451187580459-43490279c0fa?q=80&w=2072&auto=format&fit=crop');
    background-attachment: fixed;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
  }

  .hero-section h1 {
    font-size: 4em;
    margin-bottom: 10px;
    text-transform: uppercase;
    letter-spacing: 5px;
    font-weight: 800;
  }

  .profile-img {
    width: 220px;
    height: 220px;
    border-radius: 50%;
    border: 4px solid #00d4ff;
    margin: 20px 0;
    object-fit: cover;
    box-shadow: 0 0 20px rgba(0,212,255,0.5);
  }

  .skills-text {
    font-size: 1.8em;
    font-weight: 300;
    color: #e0e0e0;
    margin-bottom: 30px;
  }

  .scroll-down {
    font-size: 2.5em;
    color: white;
    text-decoration: none;
    transition: 0.3s;
    cursor: pointer;
    animation: bounce 2s infinite;
  }

  @keyframes bounce {
    0%, 20%, 50%, 80%, 100% {transform: translateY(0);}
    40% {transform: translateY(-10px);}
    60% {transform: translateY(-5px);}
  }

  .projects-section {
    padding: 80px 20px;
    background: #121212;
    color: white;
    position: relative;
    z-index: 2;
  }
</style>

<div class="hero-section">
  <h1>Bar Kazir Portfolio</h1>
  
  <img src="https://github.com/DataCropsHarvest.png" class="profile-img" alt="Bar Kazir">
  
  <p class="skills-text">Python, SQL, AI and Machine Learning</p>
  
  <a href="#projects" class="scroll-down">
    <i class="fas fa-chevron-down"></i>
  </a>
</div>

<div id="projects" class="projects-section">
  <div style="max-width: 800px; margin: 0 auto;">
    <h2 style="font-size: 2.5em; border-bottom: 2px solid #00d4ff; padding-bottom: 10px;">Projects</h2>
    
    <div style="margin-top: 40px;">
      <h3>🏠 Yad2 Smart Hunter</h3>
      <p>Automated real-estate monitoring pipeline.</p>
      <a href="https://github.com/DataCropsHarvest/Yad2-Automation" style="color: #00d4ff;">View Project on GitHub</a>
    </div>
  </div>
</div>
