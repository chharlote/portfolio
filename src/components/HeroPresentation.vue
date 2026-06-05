<template>
  <section id="accueil" class="hero">

    <div class="hero-header">
      <span class="subtitle">Développeuse back-end</span>
      <h1>Bonjour, moi c'est Charlotte</h1>
    </div>

    <div class="hero-intro">
      <div class="hero-image">
        <img src="/img/charlotte_portfolio.jpg" alt="photo profil">
      </div>

      <div class="hero-description">
        <p>
          Bonjour, je suis Charlotte, développeuse logicielle passionnée, actuellement en alternance. <br><br>
          Forte de mes expériences dans la création d'applications web et de systèmes back-end, j'attache une grande importance
          à la création d'un code propre, sécurisé et respectueux des conventions de développement.<br>
          J'aime relever des défis techniques en équipe lors d'événements comme la Nuit de l'Info.
          <br><br> Mon socle technique s'étend sur plusieurs domaines, incluant le développement Back-end (Java/SpringBoot, Node.js), l'architecture de bases de données
          (PostgreSQL) et la création d'interfaces Front-end (Vue.js). La majorité de mon code source est d'ailleurs accessible sur mon profil GitHub.
        </p>
      </div>
    </div>

    <div class="hero-actions">

      <div class="social-links">

        <a href="https://www.linkedin.com/in/charlotte-germea600081a4/" target="_blank" class="social-btn">
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"></path><rect x="2" y="9" width="4" height="12"></rect><circle cx="4" cy="4" r="2"></circle></svg>
          LinkedIn
        </a>

        <a href="https://github.com/chharlote" target="_blank" class="social-btn">
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M15 22v-4a4.8 4.8 0 0 0-1-3.2c3-.3 6-1.5 6-6.5a4.6 4.6 0 0 0-1.3-3.2 4.2 4.2 0 0 0-.1-3.2s-1.1-.3-3.5 1.3a12.3 12.3 0 0 0-6.2 0C6.5 2.8 5.4 3.1 5.4 3.1a4.2 4.2 0 0 0-.1 3.2A4.6 4.6 0 0 0 4 9.5c0 5 3 6.2 6 6.5a4.8 4.8 0 0 0-1 3.2v4"></path></svg>
          GitHub
        </a>

        <a href="portfolio/public/cv_c_germe.pdf" target="_blank" class="social-btn">
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"></path><polyline points="14 2 14 8 20 8"></polyline><line x1="16" y1="13" x2="8" y2="13"></line><line x1="16" y1="17" x2="8" y2="17"></line><polyline points="10 9 9 9 8 9"></polyline></svg>
          Mon CV
        </a>

      </div>


     <a href="#projets" class="btn"> Voir mes projets</a>


    </div>

  </section>
</template>

<style scoped>
.hero {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 80px 20px;
  max-width: 1000px;
  margin: 0 auto;
}

.hero-header {
  text-align: center;
  margin-bottom: 50px;
}

.subtitle {
  color: var(--rose-dark);
  font-weight: 600;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  font-size: 14px;
}

.hero-header h1 {
  font-size: 42px;
  margin-top: 15px;
  margin-bottom: 0;
  color: var(--texte-principal);
}

.hero-intro {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 50px;
  margin-bottom: 50px;
}

.hero-image {
  flex-shrink: 0;
}

.hero-image img {
  width: 250px;
  border-radius: 20%;
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.05);
  object-fit: cover;
}

.hero-description {
  max-width: 600px;
  text-align: left;
}

.hero-description p {
  font-size: 18px;
  line-height: 1.6;
  color: var(--texte-secondaire);
  margin: 0;
  text-align: justify;
}

.hero-actions {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
}

.social-links {
  display: flex;
  gap: 20px;
  flex-wrap: wrap;
  justify-content: center;
  margin-bottom: 40px;
}

.social-links {
  display: flex;
  gap: 20px;
  flex-wrap: wrap;
  justify-content: center;
  margin-bottom: 40px;
}

.social-btn {
  display: flex;
  align-items: center;
  gap: 10px;
  background-color: transparent;
  color: var(--rose);
  border: 2px solid var(--rose);
  padding: 10px 24px;
  border-radius: 8px;
  text-decoration: none;
  font-weight: 600;
  font-size: 16px;
  transition: all 0.3s ease;
}

.social-btn svg {
  stroke: currentColor;
}

.social-btn:hover {
  background-color: var(--rose);
  color: white;
  transform: scale(1.05);
}


.tech-stack h3 {
  font-size: 16px;
  color: var(--texte-secondaire);
  margin-bottom: 15px;
  font-weight: 500;
}


.btn {
  display: inline-block;
  padding: 12px 28px;
  background-color: var(--rose);
  color: white;
  border-radius: 8px;
  text-decoration: none;
  font-weight: 600;
  font-size: 16px;
  transition: all 0.3s ease;
}

.btn:hover {
  background-color: var(--rose-dark);
  transform: scale(1.05);
}

@media (max-width: 850px) {
  .hero-intro {
    flex-direction: column;
    text-align: center;
    gap: 30px;
  }

  .hero-description {
    text-align: center;
  }
}
</style>