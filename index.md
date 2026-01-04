---
layout: single
classes: wide
author_profile: false
---

<style>
  /* 1. מחיקת הסרגל העליון והאלמנטים המובנים של התבנית */
  .masthead, .page__footer, .page__taxonomy, .breadcrumb {
    display: none !important;
  }

  body, html {
    margin: 0;
    padding: 0;
    width: 100%;
    height: 100%;
    overflow-x: hidden;
    /* מוודא שהדף לא יבצע קפיצות מוזרות */
    scroll-behavior: auto !important; 
  }

  /* 2. פריסת הרקע על כל המסך */
  .hero-wrapper {
    position: relative;
    height: 100vh;
    width: 100vw;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    color: white;
    background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), 
                url('https://images.unsplash.com/photo-1451187580459-43490279c0fa?q=80&w=2072&auto=format&fit=crop');
    background-attachment: fixed;
    background-position: center;
    background-size: cover;
    text-align: center;
    margin-left: calc(-50vw + 50%);
  }

  h1.main-title {
    font-size: clamp(3em, 10vw, 6em);
    margin: 0;
    text-transform: uppercase;
    letter-spacing: 10px;
    font-weight: 900;
    text-shadow: 2px 2px 10px rgba(0,0,0,0.8);
  }

  /* 3. הגדלת תמונת הפרופיל */
  .profile-circle {
    width: 280px;
    height: 280px;
    border-radius: 50%;
    border: 6px solid #00d4ff;
    margin: 40px 0;
    box-shadow: 0 0 40px rgba(0, 212, 255, 0.6);
    object-fit: cover;
  }

  .skills-tagline {
    font-size: 2em;
    color: #00d4ff;
    font-weight: 300;
    letter-spacing: 2px;
    text-shadow: 1px 1px 5px rgba(0,0,0,0.5);
  }

  .scroll-arrow {
    position: absolute;
    bottom: 40px;
    font-size: 3em;
    color: white;
    animation: bounce 2s infinite;
    cursor: pointer;
    text-decoration: none;
  }

  @keyframes bounce {
    0%, 20%, 50%, 80%, 100% {transform: translateY(0);}
    40% {transform: translateY(-20px);}
    60% {transform: translateY(-10px);}
  }

  .content-section {
    background: #121212;
    padding: 80px 5%;
    color: white;
    width: 100vw;
    margin-left: calc(-50vw + 50%);
  }

  .contact-grid {
    display: flex;
    justify-content: center;
    gap: 50px;
    flex-wrap: wrap;
    margin-top: 60px;
  }

  .contact-item {
    text-align: center;
    text-decoration: none;
    color: white;
    transition: 0.4s;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .contact-item:hover {
    color: #00d4ff;
    transform: scale(1.1);
  }

  .contact-item i {
    font-size: 3.5em;
    display: block;
    margin-bottom: 15px;
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
  <div style="max-width: 1100px; margin: 0 auto;">
    <h2 style="text-align: center; font-size: 3.5em; margin-bottom: 70px; border-bottom: 2px solid #333; padding-bottom: 20px;">Projects</h2>
    
    <div style="background: #1a1a1a; padding: 40px; border-radius: 15px; border-left: 8px solid #00d4ff; margin-bottom: 100px;">
      <h3 style="font-size: 2.2em; margin-top: 0;">🏠 Yad2 Smart Hunter</h3>
      <p style="font-size: 1.2em; line-height: 1.6;">Automated monitoring pipeline for real-estate market. Scrapes, filters, and notifies in real-time.</p>
      <a href="https://github.com/DataCropsHarvest/Yad2-Automation" style="color: #00d4ff; font-weight: bold; text-decoration: none;">[ VIEW CODE ON GITHUB ]</a>
    </div>

    <h2 style="text-align: center; font-size: 3.5em; margin-top: 100px;">Get In Touch</h2>
    
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

<script>
  window.onbeforeunload = function () {
    window.scrollTo(0, 0);
  }
  history.scrollRestoration = "manual";
</script>
