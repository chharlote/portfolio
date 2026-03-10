<template>
  <section class="home-projects">
    <h2>Quelques-uns de mes projets</h2>

    <div class="projects-grid">

      <div class="project-card">
        <div class="img-placeholder">img</div>
        <h3>Titre projet 1</h3>
        <p>Une petite description du projet pour expliquer ce que c'est et les technos utilisées.</p>
        <button class="btn-projet">Voir le projet</button>
      </div>

      <div class="project-card">
        <div class="img-placeholder">img</div>
        <h3>Titre projet 2</h3>
        <p>Une petite description du projet pour expliquer ce que c'est et les technos utilisées.</p>
        <button class="btn-projet">Voir le projet</button>
      </div>

      <div class="project-card">
        <div class="img-placeholder">img</div>
        <h3>Titre projet 3</h3>
        <p>Une petite description du projet pour expliquer ce que c'est et les technos utilisées.</p>
        <button class="btn-projet">Voir le projet</button>
      </div>

    </div>
  </section>
</template>

<style scoped>
.home-projects {
  padding: 60px 20px;
  text-align: center;
}

.home-projects h2 {
  color: var(--rose-dark); /* Utilise la variable de ton styles.css */
  margin-bottom: 40px;
  font-size: 32px;
}

.projects-grid {
  display: flex;
  justify-content: center;
  gap: 30px; /* Espace entre les cartes */
  flex-wrap: wrap; /* Permet de passer à la ligne sur les petits écrans */
}

/* --- Le style de la carte --- */
.project-card {
  background: white;
  width: 300px;
  padding: 20px;
  border-radius: 15px;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.05); /* Ombre douce */
  display: flex;
  flex-direction: column;
  align-items: center;

  /* C'est ici que la magie de l'animation opère : */
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

/* L'effet de zoom (grossissement) au passage de la souris ! */
.project-card:hover {
  transform: scale(1.05); /* Grossit la carte de 5% */
  box-shadow: 0 10px 25px rgba(201, 124, 138, 0.2); /* Accentue l'ombre en rose */
}

/* --- L'image (en attendant tes vraies images) --- */
.img-placeholder {
  width: 100%;
  height: 160px;
  background-color: #f0f0f0;
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #888;
  font-weight: bold;
  margin-bottom: 15px;
}

.project-card h3 {
  color: #333;
  margin-bottom: 10px;
}

.project-card p {
  color: #666;
  font-size: 14px;
  margin-bottom: 20px;
  flex-grow: 1;
}

.btn-projet {
  background-color: transparent;
  color: var(--rose);
  border: 2px solid var(--rose);
  padding: 8px 20px;
  border-radius: 8px;
  font-weight: bold;
  cursor: pointer;
  transition: all 0.2s ease;
}

.btn-projet:hover {
  background-color: var(--rose);
  color: white;
}
</style>