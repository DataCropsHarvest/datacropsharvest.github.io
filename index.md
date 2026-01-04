---
layout: single
classes: wide
author_profile: false
---

<style>
  /* 1. איפוס מוחלט של כל רווחי התבנית */
  .masthead, .page__footer, .page__taxonomy, .breadcrumb, .page__sidebar, .archive {
    display: none !important;
  }

  /* ביטול השוליים של מיכלי התוכן המובנים */
  #main, .page, .page__content, .layout--single {
    padding: 0 !important;
    margin: 0 !important;
    max-width: 100% !important;
    width: 100% !important;
  }

  /* ביטול הרווח הלבן למעלה ומשמאל */
  body, html {
    margin: 0 !important;
    padding: 0 !important;
    width: 100vw !important;
    overflow-x: hidden;
  }

  /* 2. פריסת הרקע על כל המסך מקצה לקצה */
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
    /* התיקון הקריטי למרכוז וביטול ה-Sidebar הבלתי נראה */
    left: 50%;
    right: 50%;
    margin-left: -50vw;
    margin-right: -50vw;
  }

  h1.main-title {
    font-size: clamp(3em, 10vw, 6em);
    margin: 0;
    text-transform: uppercase;
    letter-spacing: 10px;
    font-weight: 900;
  }

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
  }

  /* 3. סקשן Projects - רקע שקוף ומרכוז */
  .content-section {
    background: rgba(18, 18, 18, 0.7); /* שקיפות משופרת */
    backdrop-filter: blur(10px);
    padding: 80px 5%;
    color: white;
    width: 100vw;
    position: relative;
    left: 50%;
    right: 50%;
    margin-left: -50vw;
    margin-right: -50vw;
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
    width: 120px;
  }

  .contact-item i {
    font-size: 3.5em;
    display: block;
    margin-bottom: 15px;
  }

  .scroll-arrow {
    position: absolute;
    bottom: 40px;
    font-size: 3em;
    color: white;
    animation: bounce 2s infinite;
    cursor: pointer;
  }

  @keyframes bounce {
    0%, 20%, 50%, 80%, 100% {transform: translateY(0);}
    40% {transform: translateY(-20px);}
    60% {transform: translateY(-10px);}
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
    
    <div style="background: rgba(255,255,255,0.05); padding: 40px; border-radius: 15px; border-left: 8px solid #00d4ff; margin-bottom: 100px;">
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
  if ('scrollRestoration' in history) { history.scrollRestoration = 'manual'; }
  window.scrollTo(0, 0);
</script>
