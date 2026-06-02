<template>
  <section id="parcours" class="parcours-section">
    <h2>Mon Parcours</h2>
    <p class="intro-text">Découvrez mon évolution professionnelle et académique.</p>

    <div class="timelines-container">

      <div class="timeline">
        <h3>Expériences Professionnelles</h3>

        <div class="timeline-item">
          <div class="timeline-dot"></div>
          <div class="timeline-content">
            <span class="date">2024 - Présent</span>
            <h4>Développeuse Back-end</h4>
            <span class="place">SNCF Connect & Tech - Lille</span>
            <p> ▸ Développement et maintenance de services back-end
              en Java / Spring Boot.<br>
              ▸ Développement et maintenance d’API REST et d’IHM. <br>
              ▸ Création d’un outil de génération de token en python. <br>
              ▸ Travail en équipe SCRUM.<br>
              ▸ Logiciels utilisés : Git, IntellIJ, Postman</p>
          </div>
        </div>

        <div class="timeline-item">
          <div class="timeline-dot"></div>
          <div class="timeline-content">
            <span class="date">Été 2023</span>
            <h4>Assistante de gestion des stocks</h4>
            <span class="place"> ACIME FRAME - Rinxent </span>
            <p>▸ Réalisation d'inventaires à l'aide d'outils informatiques de gestion.<br>
            ▸ Optimisation et réorganisation physique de l'espace de stockage.</p>
          </div>
        </div>
      </div>

      <div class="timeline">
        <h3>Formation</h3>

        <div class="timeline-item">
          <div class="timeline-dot"></div>
          <div class="timeline-content">
            <span class="date">2023 - 2026</span>
            <h4>BUT Informatique</h4>
            <span class="place">IUT du Littoral de la Côte d'Opale - Calais</span>
            <p> ▸ Parcours réalisation d'applications : conception, développement, validation. <br>
              ▸ Réalistation de projet seul ou en groupe.<br>
              ▸ Apprentissage des langages : C, python, JAVA, Vue.js, PHP, Node.js, C++ <br>
              ▸ Logiciels utilisés : Git, VisualStudioCode, Wamp</p>
          </div>
        </div>

        <div class="timeline-item">
          <div class="timeline-dot"></div>
          <div class="timeline-content">
            <span class="date">2020 - 2023</span>
            <h4>Baccalauréat Général</h4>
            <span class="place">Lycée Edouard Branly - Boulogne-sur-Mer</span>
            <p>Spécialité Mathématiques et Physique-Chimie. <br>Section européenne anglais.<br>Mention Bien.</p>
          </div>
        </div>
      </div>

    </div>

    <div class="cv-container">
      <a href="../assets/cv_c_germe.pdf" target="_blank" class="btn-cv" download>
        📄 Télécharger mon CV
      </a>
    </div>
  </section>
</template>

<style scoped>
.parcours-section {
  padding: 80px 20px;
  background-color: var(--fond-element); /* Fond blanc pour alterner avec le gris de l'accueil */
  text-align: center;
}

.parcours-section h2 {
  color: var(--rose-dark);
  font-size: 32px;
  margin-bottom: 10px;
}

.intro-text {
  color: var(--texte-secondaire);
  margin-bottom: 50px;
  font-size: 18px;
}

.timelines-container {
  display: flex;
  justify-content: center;
  gap: 60px;
  max-width: 1000px;
  margin: 0 auto;
  flex-wrap: wrap; /* Permet de passer les colonnes l'une sous l'autre sur téléphone */
}

.timeline {
  flex: 1;
  min-width: 300px; /* Largeur minimum avant de passer à la ligne */
  text-align: left;
}

.timeline h3 {
  color: var(--texte-principal);
  font-size: 22px;
  margin-bottom: 30px;
  display: flex;
  align-items: center;
  gap: 10px;
}

/* --- La ligne du temps --- */
.timeline-item {
  position: relative;
  padding-left: 30px; /* Laisse de la place pour la ligne */
  margin-bottom: 40px;
  border-left: 2px solid var(--rose); /* C'est ça la fameuse ligne verticale ! */
}

/* Le petit point sur la ligne */
.timeline-dot {
  position: absolute;
  left: -7px; /* Centre le point sur la ligne de 2px */
  top: 0;
  width: 12px;
  height: 12px;
  background-color: var(--rose-dark);
  border-radius: 50%;
  box-shadow: 0 0 0 4px var(--fond-element); /* Crée un espace blanc autour du point */
}

.timeline-content {
  background: var(--fond-page);
  padding: 20px;
  border-radius: 12px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.03);
  transition: transform 0.3s ease;
}

.timeline-content:hover {
  transform: translateX(5px); /* Décale légèrement la boîte vers la droite au survol */
}

.date {
  color: var(--rose-dark);
  font-weight: 600;
  font-size: 14px;
}

.timeline-content h4 {
  color: var(--texte-principal);
  font-size: 18px;
  margin: 8px 0 4px 0;
}

.place {
  color: #888;
  font-size: 14px;
  font-style: italic;
  display: block;
  margin-bottom: 10px;
}

.timeline-content p {
  color: var(--texte-secondaire);
  font-size: 15px;
  line-height: 1.5;
  margin: 0;
}

/* --- Bouton CV --- */
.cv-container {
  margin-top: 60px;
}

.btn-cv {
  display: inline-block;
  padding: 14px 30px;
  background-color: white;
  color: var(--rose-dark);
  border: 2px solid var(--rose);
  border-radius: 8px;
  text-decoration: none;
  font-weight: 600;
  font-size: 16px;
  transition: all 0.3s ease;
  box-shadow: 0 4px 10px rgba(232, 160, 173, 0.1);
}

.btn-cv:hover {
  background-color: var(--rose);
  color: white;
  transform: translateY(-3px);
  box-shadow: 0 6px 15px rgba(232, 160, 173, 0.3);
}
</style>
<script setup lang="ts">
</script>