---
layout: single
classes: wide
author_profile: false
---

<style>
  /* 1. ביטול אלמנטים מובנים */
  .masthead, .page__footer, .page__taxonomy, .breadcrumb, .page__sidebar, .page__title {
    display: none !important;
  }

  #main, .page, .page__content, .archive {
    width: 100% !important; max-width: 100% !important; padding: 0 !important; margin: 0 !important;
  }

  body, html {
    margin: 0 !important; padding: 0 !important; width: 100vw !important; overflow-x: hidden;
    scroll-behavior: smooth;
  }

  /* 2. Hero Section */
  .hero-wrapper {
    position: relative; height: 100vh; width: 100vw; display: flex; flex-direction: column;
    align-items: center; justify-content: center; color: white;
    background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), 
                url('https://images.unsplash.com/photo-1451187580459-43490279c0fa?q=80&w=2072&auto=format&fit=crop');
    background-attachment: fixed; background-position: center; background-size: cover;
    left: 50%; transform: translateX(-50%); text-align: center;
  }

  .profile-circle {
    width: clamp(180px, 40vw, 280px); height: clamp(180px, 40vw, 280px);
    border-radius: 50%; border: 6px solid #00d4ff; margin: 20px 0;
    box-shadow: 0 0 40px rgba(0, 212, 255, 0.6); object-fit: cover;
  }

  /* 3. סקשן התוכן */
  .content-wrapper {
    background: rgba(18, 18, 18, 0.9); backdrop-filter: blur(15px); color: white;
    width: 100vw; position: relative; left: 50%; transform: translateX(-50%);
    padding: 40px 0 80px 0; display: flex; flex-direction: column; align-items: center;
  }

  .container { width: 95%; max-width: 1200px; margin: 0 auto; }

  .project-card {
    background: rgba(255, 255, 255, 0.05); border-radius: 15px; padding: 25px;
    border: 1px solid rgba(0, 212, 255, 0.2); margin-bottom: 30px; text-align: left;
    max-width: 700px; margin-left: auto; margin-right: auto;
  }

  .tech-tag {
    display: inline-block; background: rgba(0, 212, 255, 0.1); color: #00d4ff;
    padding: 3px 10px; border-radius: 5px; font-size: 0.75em; margin: 3px 5px 3px 0; border: 1px solid #00d4ff;
  }

  /* 4. עיצוב אייקונים תחתון - ריווח מקסימלי מורחב */
  .contact-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr); 
    gap: 40px; 
    margin: 60px auto 0 auto;
    width: 100%;
    max-width: 1100px; /* ריווח רחב מאוד */
    justify-items: center;
  }

  .contact-item {
    color: white !important;
    text-align: center;
    text-decoration: none;
    transition: 0.3s;
    display: flex;
    flex-direction: column;
    align-items: center;
    white-space: nowrap;
  }

  a.contact-item:hover {
    color: #00d4ff !important;
    transform: scale(1.05);
  }
  
  .contact-item i { font-size: 3.2em; margin-bottom: 15px; }
  .contact-label { font-weight: bold; font-size: 1.05em; display: block; }

  .scroll-arrow {
    position: absolute; bottom: 40px; font-size: 3em; color: white; animation: bounce 2s infinite;
  }

  /* התאמה למובייל */
  @media (max-width: 900px) {
    .contact-grid {
      grid-template-columns: repeat(2, 1fr);
      gap: 40px;
      max-width: 500px;
    }
    .contact-item { white-space: normal; }
  }

  @keyframes bounce { 0%, 20%, 50%, 80%, 100% {transform: translateY(0);} 40% {transform: translateY(-20px);} 60% {transform: translateY(-10px);} }
</style>

<div class="hero-wrapper">
  <h1 style="font-size: clamp(3em, 10vw, 5em); text-transform: uppercase; margin: 0; letter-spacing: 5px; font-weight: 900;">Bar Kazir Portfolio</h1>
  <img src="https://github.com/DataCropsHarvest.png" class="profile-circle" alt="Bar Kazir">
  <p style="font-size: 2em; color: #00d4ff; font-weight: 300;">Python | SQL | AI and Machine Learning</p>
  <a href="#projects" class="scroll-arrow"><i class="fas fa-chevron-down"></i></a>
</div>

<div id="projects" class="content-wrapper">
  <div class="container">
    <h2 style="text-align: center; font-size: 2.8em; margin: 0 0 40px 0;">Projects</h2>

    {% if site.data.projects %}
      {% for project in site.data.projects %}
      <div class="project-card">
        {% if project.image %}
        <img src="{{ project.image }}" style="width: 100%; max-height: 300px; object-fit: cover; border-radius: 10px; margin-bottom: 15px; border: 1px solid rgba(0,212,255,0.1);">
        {% endif %}
        
        <h3 style="font-size: 1.6em; color: #00d4ff; margin-top: 0; margin-bottom: 10px;">{{ project.title }}</h3>
        <p style="font-size: 1em; line-height: 1.5; margin-bottom: 15px;">{{ project.description }}</p>
        
        <div style="margin: 15px 0;">
          {% for tag in project.tech %}
          <span class="tech-tag">{{ tag }}</span>
          {% endfor %}
        </div>
        
        <a href="{{ project.link }}" target="_blank" style="color: #00d4ff; font-size: 0.9em; font-weight: bold; text-decoration: none; border: 1px solid #00d4ff; padding: 8px 16px; border-radius: 5px; display: inline-block;">VIEW PROJECT →</a>
      </div>
      {% endfor %}
    {% endif %}

    <h2 style="text-align: center; font-size: 3em; margin-top: 80px;">Get In Touch</h2>
    <div class="contact-grid">
      <a href="https://wa.me/972547869012" class="contact-item" target="_blank">
        <i class="fab fa-whatsapp"></i>
        <span class="contact-label">(+972)-54-7869012</span>
      </a>

      <div class="contact-item">
        <i class="fas fa-envelope"></i>
        <span class="contact-label">barkazir@gmail.com</span>
      </div>

      <a href="https://www.linkedin.com/in/bar-kazir/" class="contact-item" target="_blank">
        <i class="fab fa-linkedin"></i>
        <span class="contact-label">LinkedIn</span>
      </a>

      <a href="https://github.com/DataCropsHarvest" class="contact-item" target="_blank">
        <i class="fab fa-github"></i>
        <span class="contact-label">GitHub</span>
      </a>
    </div>
  </div>
</div>

<script>
  window.onbeforeunload = function () { window.scrollTo(0, 0); };
  if ('scrollRestoration' in history) { history.scrollRestoration = 'manual'; }
  window.scrollTo(0, 0);
</script>
