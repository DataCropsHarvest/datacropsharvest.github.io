---
layout: single
classes: wide
author_profile: false
---

<style>
  /* 1. מחיקת כל השאריות של התבנית המובנית שכופות הטיה ימינה */
  .masthead, .page__footer, .page__taxonomy, .breadcrumb, .page__sidebar, .page__title {
    display: none !important;
  }

  /* ביטול הגבלת הרוחב של Jekyll */
  #main, .page, .page__content, .archive {
    width: 100% !important;
    max-width: 100% !important;
    padding: 0 !important;
    margin: 0 !important;
  }

  /* הבטחה שהתוכן לא יזוז ימינה */
  .layout--single .page__content {
    float: none !important;
    width: 100% !important;
    padding-right: 0 !important;
  }

  body, html {
    margin: 0 !important;
    padding: 0 !important;
    width: 100vw !important;
    overflow-x: hidden;
  }

  /* 2. Hero Section - מרכוז אבסולוטי */
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
    /* טריק המרכוז הקריטי */
    left: 50%;
    transform: translateX(-50%);
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

  /* 3. סקשן התוכן */
  .content-wrapper {
    background: rgba(18, 18, 18, 0.9);
    backdrop-filter: blur(15px);
    color: white;
    width: 100vw;
    position: relative;
    left: 50%;
    transform: translateX(-50%);
    padding: 80px 0;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .container {
    width: 90%;
    max-width: 900px;
    margin: 0 auto;
  }

  .project-card {
    background: rgba(255, 255, 255, 0.05);
    border-radius: 15px;
    padding: 35px;
    border: 1px solid rgba(0, 212, 255, 0.2);
    margin-bottom: 40px;
    text-align: left;
  }

  .tech-tag {
    display: inline-block;
    background: rgba(0, 212, 255, 0.1);
    color: #00d4ff;
    padding: 4px 12px;
    border-radius: 5px;
    font-size: 0.85em;
    margin: 5px 5px 5px 0;
    border: 1px solid #00d4ff;
  }

  .contact-grid {
    display: flex;
    justify-content: center;
    gap: 50px;
    flex-wrap: wrap;
    margin-top: 50px;
    width: 100%;
  }

  .contact-item {
    color: white;
    text-align: center;
    text-decoration: none;
    transition: 0.3s;
  }

  .contact-item:hover { color: #00d4ff; transform: scale(1.1); }
  .contact-item i { font-size: 3em; display: block; margin-bottom: 10px; }

  .scroll-arrow {
    position: absolute;
    bottom: 40px;
    font-size: 3em;
    color: white;
    animation: bounce 2s infinite;
  }

  @keyframes bounce {
    0%, 20%, 50%, 80%, 100% {transform: translateY(0);}
    40% {transform: translateY(-20px);}
    60% {transform: translateY(-10px);}
  }
</style>

<div class="hero-wrapper">
  <h1 style="font-size: clamp(3em, 10vw, 5em); text-transform: uppercase; margin: 0; letter-spacing: 10px; font-weight: 900;">Bar Kazir</h1>
  <img src="https://github.com/DataCropsHarvest.png" class="profile-circle" alt="Bar Kazir">
  <p style="font-size: 2em; color: #00d4ff; font-weight: 300;">Python | SQL | AI and Machine Learning</p>
  <a href="#projects" class="scroll-arrow"><i class="fas fa-chevron-down"></i></a>
</div>

<div id="projects" class="content-wrapper">
  <div class="container">
    <h2 style="text-align: center; font-size: 3.5em; margin-bottom: 60px;">Featured Projects</h2>

    {% if site.data.projects %}
      {% for project in site.data.projects %}
      <div class="project-card">
        {% if project.image %}
        <img src="{{ project.image }}" style="width: 100%; border-radius: 10px; margin-bottom: 20px; border: 1px solid rgba(0,212,255,0.1);">
        {% endif %}
        
        <h3 style="font-size: 2.2em; color: #00d4ff; margin-top: 0;">{{ project.title }}</h3>
        <p style="font-size: 1.2em; line-height: 1.6;">{{ project.description }}</p>
        
        <div style="margin: 20px 0;">
          {% for tag in project.tech %}
          <span class="tech-tag">{{ tag }}</span>
          {% endfor %}
        </div>

        <a href="{{ project.link }}" target="_blank" style="color: #00d4ff; font-weight: bold; text-decoration: none; border: 1px solid #00d4ff; padding: 10px 20px; border-radius: 5px;">
          VIEW PROJECT →
        </a>
      </div>
      {% endfor %}
    {% endif %}

    <h2 style="text-align: center; font-size: 3.5em; margin-top: 100px;">Get In Touch</h2>
    <div class="contact-grid">
      <a href="https://wa.me/972547869012" class="contact-item" target="_blank">
        <i class="fab fa-whatsapp"></i><span>WhatsApp</span>
      </a>
      <a href="mailto:Barkazir@gmail.com" class="contact-item">
        <i class="fas fa-envelope"></i><span>Email</span>
      </a>
      <a href="https://www.linkedin.com/in/bar-kazir/" class="contact-item" target="_blank">
        <i class="fab fa-linkedin"></i><span>LinkedIn</span>
      </a>
      <a href="https://github.com/DataCropsHarvest" class="contact-item" target="_blank">
        <i class="fab fa-github"></i><span>GitHub</span>
      </a>
    </div>
  </div>
</div>

<script>
  if ('scrollRestoration' in history) { history.scrollRestoration = 'manual'; }
  window.scrollTo(0, 0);
</script>
