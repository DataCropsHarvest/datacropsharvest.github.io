---
layout: single
classes: wide
author_profile: false
---

<style>
  /* הגדרות כלליות */
  body, html {
    margin: 0;
    padding: 0;
    overflow-x: hidden;
  }

  /* סקשן ראשון - Full Screen */
  .hero-wrapper {
    position: relative;
    height: 100vh;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    color: white;
    background-image: url('https://images.unsplash.com/photo-1451187580459-43490279c0fa?q=80&w=2072&auto=format&fit=crop');
    background-attachment: fixed; /* אפקט הציפה */
    background-position: center;
    background-size: cover;
    text-align: center;
  }

  .hero-content {
    background: rgba(0, 0, 0, 0.6); /* שכבת כהות על הרקע כדי שהטקסט יבלוט */
    padding: 40px;
    border-radius: 20px;
    width: 80%; /* הרקע תופס 80% מהרוחב כפי שביקשת */
    max-width: 1200px;
  }

  h1.main-title {
    font-size: clamp(2.5em, 8vw, 5em);
    margin: 0;
    text-transform: uppercase;
    letter-spacing: 8px;
  }

  .profile-circle {
    width: 200px;
    height: 200px;
    border-radius: 50%;
    border: 5px solid #00d4ff;
    margin: 30px 0;
    box-shadow: 0 0 30px rgba(0, 212, 255, 0.4);
  }

  .skills-tagline {
    font-size: 1.8em;
    color: #00d4ff;
    font-weight: 300;
    margin-bottom: 40px;
  }

  /* חץ אנימטיבי */
  .scroll-arrow {
    position: absolute;
    bottom: 30px;
    font-size: 2em;
    color: white;
    animation: bounce 2s infinite;
    cursor: pointer;
  }

  @keyframes bounce {
    0%, 20%, 50%, 80%, 100% {transform: translateY(0);}
    40% {transform: translateY(-15px);}
    60% {transform: translateY(-7px);}
  }

  /* סקשן פרויקטים ויצירת קשר */
  .content-section {
    background: #121212;
    padding: 100px 20px;
    color: white;
  }

  .contact-grid {
    display: flex;
    justify-content: center;
    gap: 40px;
    flex-wrap: wrap;
    margin-top: 50px;
  }

  .contact-item {
    text-align: center;
    text-decoration: none;
    color: white;
    transition: 0.3s;
  }

  .contact-item:hover {
    color: #00d4ff;
    transform: translateY(-5px);
  }

  .contact-item i {
    font-size: 3em;
    display: block;
    margin-bottom: 10px;
  }
</style>

<div class="hero-wrapper">
  <div class="hero-content">
    <h1 class="main-title">Bar Kazir Portfolio</h1>
    <img src="https://github.com/DataCropsHarvest.png" class="profile-circle" alt="Bar Kazir">
    <p class="skills-tagline">Python | SQL | AI and Machine Learning</p>
  </div>
  
  <a href="#projects" class="scroll-arrow">
    <i class="fas fa-chevron-down"></i>
  </a>
</div>

<div id="projects" class="content-section">
  <div style="max-width: 1000px; margin: 0 auto;">
    <h2 style="text-align: center; font-size: 3em; margin-bottom: 60px;">Projects</h2>
    
    <div style="border-left: 4px solid #00d4ff; padding-left: 20px; margin-bottom: 80px;">
      <h3>🏠 Yad2 Smart Hunter</h3>
      <p>Real-time automation pipeline for real-estate market monitoring.</p>
      <a href="https://github.com/DataCropsHarvest/Yad2-Automation" style="color: #00d4ff;">Source Code →</a>
    </div>

    <h2 style="text-align: center; font-size: 3em; margin-top: 100px;">Get In Touch</h2>
    
    <div class="contact-grid">
      <a href="https://wa.me/972547869012" class="contact-item" target="_blank">
        <i class="fab fa-whatsapp"></i>
        <span>WhatsApp</span>
      </a>
      
      <a href="mailto:Barkazir@gmail.com" class="contact-item">
        <i class="fas fa-envelope"></i>
        <span>Email</span>
      </a>
      
      <a href="https://www.linkedin.com/in/bar-kazir/" class="contact-item" target="_blank">
        <i class="fab fa-linkedin"></i>
        <span>LinkedIn</span>
      </a>
      
      <a href="https://github.com/DataCropsHarvest" class="contact-item" target="_blank">
        <i class="fab fa-github"></i>
        <span>GitHub</span>
      </a>
    </div>
  </div>
</div>
