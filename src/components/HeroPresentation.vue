<template>
  <section class="hero">
    <div class="hero-text">
      <span class="subtitle">Développeuse back-end</span>

      <h1>Bonjour, moi c'est Charlotte</h1>

      <p class="description">
        Je conçois et développe des applications web modernes et intuitives.
        De la conception à l'intégration, j'aime résoudre des problèmes techniques
        et donner vie à des projets ambitieux.
      </p>

      <div class="tech-stack">
        <h3>Mes technos préférées :</h3>
        <div class="badges">
          <span class="badge">Vue.js</span>
          <span class="badge">JavaScript</span>
          <span class="badge">TypeScript</span>
          <span class="badge">HTML & CSS</span>
          <span class="badge">Git</span>
        </div>
      </div>

      <router-link to="/projects" class="btn">
        Voir mes projets
      </router-link>
    </div>

    <div class="hero-image">
      <img src="../assets/img/homeview.png" alt="photo profil">
    </div>
  </section>
</template>

<style scoped>

.hero {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 60px 20px;
  text-align: center;
}

.hero-text {
  max-width: 650px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

/* --- Typographie --- */
.subtitle {
  color: var(--rose-dark);
  font-weight: 600;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  font-size: 14px;
}

.hero h1 {
  font-size: 42px;
  margin-top: 15px;
  margin-bottom: 20px;
  color: var(--texte-principal);
}

.description {
  font-size: 18px;
  line-height: 1.6;
  color: var(--texte-secondaire);
  margin-bottom: 35px;
}

.tech-stack {
  margin-bottom: 35px;
}

.tech-stack h3 {
  font-size: 16px;
  color: var(--texte-secondaire);
  margin-bottom: 15px;
  font-weight: 500;
}

.badges {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 10px;
}

.badge {
  background-color: var(--fond-element, #ffffff);
  color: var(--rose-dark);
  padding: 8px 16px;
  border-radius: 20px;
  font-size: 14px;
  font-weight: 600;
  border: 1px solid var(--rose);
  transition: all 0.3s ease;
}

.badge:hover {
  background-color: var(--rose);
  color: white;
  transform: translateY(-3px);
  box-shadow: 0 4px 10px rgba(232, 160, 173, 0.3);
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

/* --- Image --- */
.hero-image {
  margin-top: 40px;
}

.hero-image img {
  width: 250px;
  border-radius: 50%;
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.05);
}
</style>