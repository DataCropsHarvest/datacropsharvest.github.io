---
layout: single
classes: wide
author_profile: false
---

<style>
  /* 1. ניקוי יסודי של אלמנטים מובנים */
  .masthead, .page__footer, .page__taxonomy, .breadcrumb, .page__sidebar {
    display: none !important;
  }

  /* ביטול שוליים כפויים של התבנית */
  #main {
    padding: 0 !important;
    margin: 0 !important;
    max-width: 100% !important;
  }

  body, html {
    margin: 0;
    padding: 0;
    width: 100%;
    overflow-x: hidden;
  }

  /* 2. סקשן הגיבור - פריסה ומרכוז פלס */
  .hero-wrapper {
    height: 100vh;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    color: white;
    background: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.4)), 
                url('https://images.unsplash.com/photo-1451187580459-43490279c0fa?q=80&w=2072&auto=format&fit=crop');
    background-attachment: fixed;
    background-position: center;
    background-size: cover;
    text-align: center;
  }

  h1.main-title {
    font-size: clamp(2.5em, 8vw, 5.5em);
    margin: 0;
    text-transform: uppercase;
    letter-spacing: 8px;
    font-weight: 900;
    width: 100%;
  }

  .profile-circle {
    width: 260px;
    height: 260px;
    border-radius: 50%;
    border: 6px solid #00d4ff;
    margin: 30px auto;
    box-shadow: 0 0 30px rgba(0, 212, 255, 0.5);
    object-fit: cover;
    display: block;
  }

  .skills-tagline {
    font-size: 1.8em;
    color: #00d4ff;
    font-weight: 300;
    margin: 0;
  }

  /* 3. סקשן Projects - רקע שקוף יותר (0.6) עם טשטוש */
  .content-section {
    background: rgba(18, 18, 18, 0.6); /* שקיפות מוגברת */
    backdrop-filter: blur(15px); /* טשטוש חזק יותר למראה יוקרתי */
    -webkit-backdrop-filter: blur(15px);
    padding: 100px 20px;
    color: white;
    width: 100%;
    min-height: 100vh;
  }

  /* 4. תיקון מרכוז האייקונים */
  .contact-grid {
    display: flex;
    justify-content: center;
    gap: 50px;
    flex-wrap: wrap;
    margin-top: 50px;
    width: 100%;
  }

  .contact-item {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    text-decoration: none;
    color: white;
    width: 120px; /* רוחב קבוע מבטיח מרכוז פנימי */
  }

  .contact-item i {
    font-size: 3.5em;
    margin-bottom: 10px;
    display: block;
  }

  .scroll-arrow {
    position: absolute;
    bottom: 30px;
    font-size: 3em;
    color: white;
    animation: bounce 2s infinite;
    text-decoration: none;
  }

  @keyframes bounce {
    0%, 20%, 50%, 80%, 100% {transform: translateY(0);}
    40% {transform: translateY(-15px);}
    60% {transform: translateY(-7px);}
  }
</style>

<div class="hero-wrapper">
  <h1 class="main-title">Bar Kazir Portfolio</h1>
  <img src="https://github.com/DataCropsHarvest.png" class="profile-circle" alt="Bar Kazir">
  <p class="skills-tagline">Python | SQL | AI and Machine Learning</p>
  
  <a href="#projects" class="scroll-arrow">
    <i class="fas fa-chevron-down"></i>
  </a>
</div>

<div id="projects" class="content-section">
  <div style="max-width: 900px; margin: 0 auto; text-align: left;">
    <h2 style="text-align: center; font-size: 3em; margin-bottom: 60px;">Projects</h2>
    
    <div style="background: rgba(255, 255, 255, 0.08); padding: 35px; border-radius: 15px; border-left: 6px solid #00d4ff; margin-bottom: 100px;">
      <h3 style="margin-top: 0; font-size: 2em;">🏠 Yad2 Smart Hunter</h3>
      <p style="font-size: 1.1em; color: #ccc;">Automated monitoring pipeline for real-estate market. Scrapes, filters, and notifies in real-time.</p>
      <a href="https://github.com/DataCropsHarvest/Yad2-Automation" style="color: #00d4ff; text-decoration: none; font-weight: bold;">[ VIEW SOURCE ]</a>
    </div>

    <h2 style="text-align: center; font-size: 3em; margin-top: 50px;">Get In Touch</h2>
    
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
