---
layout: splash
author_profile: false
---

<style>
  /* איפוס והגדרות בסיס */
  .masthead, .page__footer, .page__taxonomy, .breadcrumb, .page__sidebar {
    display: none !important;
  }
  
  #main {
    padding: 0 !important;
    margin: 0 !important;
    max-width: 100% !important;
  }

  body, html {
    margin: 0 !important;
    padding: 0 !important;
    width: 100% !important;
    overflow-x: hidden;
    background-color: #121212;
  }

  /* Hero Section */
  .hero-wrapper {
    position: relative;
    height: 100vh;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    color: white;
    background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), 
                url('https://images.unsplash.com/photo-1451187580459-43490279c0fa?q=80&w=2072&auto=format&fit=crop');
    background-attachment: fixed;
    background-position: center;
    background-size: cover;
    text-align: center;
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

  /* Content Section */
  .content-wrapper {
    background: rgba(18, 18, 18, 0.9);
    backdrop-filter: blur(15px);
    color: white;
    width: 100%;
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
    padding: 30px;
    border: 1px solid rgba(0, 212, 255, 0.2);
    margin-bottom: 40px;
    text-align: left;
  }

  .project-img {
    width: 100%;
    max-height: 400px;
    object-fit: cover;
    border-radius: 10px;
    margin-bottom: 20px;
    border: 1px solid rgba(0, 212, 255, 0.1);
  }

  .tech-tag {
    display: inline-block;
    background: rgba(0, 212, 255, 0.1);
    color: #00d4ff;
    padding: 4px 10px;
    border-radius: 5px;
    font-size: 0.8em;
    margin-right: 8px;
    border: 1px solid #00d4ff;
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

  .contact-grid {
    display: flex;
    justify-content: center;
    gap: 40px;
    flex-wrap: wrap;
    margin-top: 40px;
  }

  .contact-item {
    color: white;
    text-decoration: none;
    text-align: center;
    font-size: 1.1em;
  }
  .contact-item i { font-size: 2.5em; display: block; margin-bottom: 10px; }
  .contact-item:hover { color: #00d4ff; }
</style>

<div class="hero-wrapper">
  <h1 style="font-size: clamp(2.5em, 8vw, 5em); margin: 0; letter-spacing: 5px; font-weight: 900;">BAR KAZIR</h1>
  <img src="https://github.com/DataCropsHarvest.png" class="profile-circle" alt="Bar Kazir">
  <p style="font-size: 1.8em; color: #00d4ff; font-weight: 300;">Python | SQL | AI and Machine Learning</p>
  <a href="#projects" class="scroll-arrow"><i class="fas fa-chevron-down"></i></a>
</div>

<div id="projects" class="content-wrapper">
  <div class="container">
    <h2 style="text-align: center; font-size: 3em; margin-bottom: 50px;">Featured Projects</h2>

    {% if site.data.projects %}
      {% for project in site.data.projects %}
      <div class="project-card">
        {% if project.image %}
        <img src="{{ project.image | relative_url }}" alt="{{ project.title }}" class="project-img">
        {% endif %}
        
        <h3 style="font-size: 2em; color: #00d4ff; margin-top: 0;">{{ project.title }}</h3>
        <p style="font-size: 1.1em; line-height: 1.6;">{{ project.description }}</p>
        
        <div style="margin: 15px 0;">
          {% for tag in project.tech %}
          <span class="tech-tag">{{ tag }}</span>
          {% endfor %}
        </div>

        <a href="{{ project.link }}" target="_blank" style="color: #00d4ff; font-weight: bold; text-decoration: none; border-bottom: 1px dashed #00d4ff;">
          VIEW PROJECT →
        </a>
      </div>
      {% endfor %}
    {% else %}
