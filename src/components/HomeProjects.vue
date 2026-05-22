<template>
  <section id="projets" class="home-projects">
    <h2>Mes Projets</h2>
    <p class="intro-text">Voici une sélection de mes réalisations les plus significatives.</p>

    <div class="projects-grid">

      <div class="project-card">
        <div class="img-placeholder"><img src="../assets/img/skyrift.png" alt="skyrift"></div>

        <div class="project-techs">
          <span class="tech-mini-badge">Python</span>
          <span class="tech-mini-badge">Pyagme</span>
        </div>

        <h3>Skyrift</h3>
        <p>
          Description détaillée du projet. Comme il n'y a plus de page dédiée,
          vous pouvez expliquer ici les fonctionnalités principales, le contexte
          (scolaire ou personnel) et les défis techniques que vous avez relevés.
        </p>

        <a href="LIEN_GITHUB_OU_SITE" target="_blank" class="btn-projet">Voir le projet</a>
      </div>

      <div class="project-card">
        <div class="img-placeholder"><img src="../assets/img/swagger-tennis.png" alt="swagger-tennis"></div>

        <div class="project-techs">
          <span class="tech-mini-badge">Node.js</span>
          <span class="tech-mini-badge">TypeScript </span>
          <span class="tech-mini-badge">PostgreSQL </span>

        </div>

        <h3>API Tennis</h3>
        <p>
          ▸ Élaboration de l’API en Node.js<br>
          ▸ Création de tests d’intégration avec POSTMAN<br>
          ▸ Réalisation de la documentation avec Swagger<br>
          ▸ Création de la base de données PostgreSQL à laquelle fait appel l’API<br>
        </p>

        <a href="https://github.com/chharlote/api_tennis" target="_blank" class="btn-projet">Lien Github</a>
      </div>

    </div>
  </section>
</template>

<style scoped>
.home-projects {
  padding: 80px 20px;
  background-color: var(--fond-page);
  text-align: center;
}

.home-projects h2 {
  color: var(--rose-dark);
  margin-bottom: 10px;
  font-size: 32px;
}

.intro-text {
  color: var(--texte-secondaire);
  margin-bottom: 50px;
  font-size: 18px;
}

.projects-grid {
  display: flex;
  justify-content: center;
  gap: 40px;
  flex-wrap: wrap;
  max-width: 1100px;
  margin: 0 auto;
}

.project-card {
  background: var(--fond-element);
  width: 480px;
  max-width: 100%;
  padding: 25px;
  border-radius: 15px;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.05);
  display: flex;
  flex-direction: column;
  align-items: center;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.project-card:hover {
  transform: scale(1.03);
  box-shadow: 0 10px 25px rgba(201, 124, 138, 0.2);
}

.img-placeholder {
  width: 100%;
  height: 220px;
  background-color: #f0f0f0;
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #888;
  font-weight: bold;
  margin-bottom: 20px;
}

.project-techs {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 8px;
  margin-bottom: 15px;
}

.tech-mini-badge {
  background-color: var(--fond-page);
  color: var(--texte-secondaire);
  font-size: 12px;
  font-weight: 600;
  padding: 4px 12px;
  border-radius: 12px;
  border: 1px solid #eaeaea;
}

.project-card h3 {
  color: var(--texte-principal);
  font-size: 22px;
  margin-bottom: 15px;
}

.project-card p {
  color: var(--texte-secondaire);
  font-size: 15px;
  line-height: 1.6;
  margin-bottom: 25px;
  flex-grow: 1;
}

.btn-projet {
  display: inline-block;
  background-color: transparent;
  color: var(--rose);
  border: 2px solid var(--rose);
  padding: 10px 24px;
  border-radius: 8px;
  font-weight: 600;
  text-decoration: none;
  transition: all 0.2s ease;
}

.btn-projet:hover {
  background-color: var(--rose);
  color: white;
}

.img-placeholder {
  width: 100%;
  height: 220px;
  border-radius: 10px;
  margin-bottom: 20px;
  overflow: hidden;
}

.img-placeholder img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.5s ease;
}

.project-card:hover .img-placeholder img {
  transform: scale(1.1);
}

.project-card p {
  color: var(--texte-secondaire);
  font-size: 15px;
  line-height: 1.6;
  margin-bottom: 25px;
  flex-grow: 1;

  text-align: left;
  width: 100%;
}
</style>
<script setup lang="ts">
</script>