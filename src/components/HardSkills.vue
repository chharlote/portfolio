<template>
  <section id="competences" class="skills-section">

    <div class="skills-header">
      <h2>Mes Hard Skills</h2>
      <p>Grâce à ma formation et mon expérience, j'ai acquis de solides compétences techniques.</p>
    </div>

    <div class="skills-container">

      <div class="skill-category" v-for="(category, index) in groupedSkills" :key="index">
        <h3 class="category-title">{{ category.titre }}</h3>

        <div class="skills-grid">

          <div class="skill-item" v-for="skill in category.competences" :key="skill.nom">

            <div class="icon-ring" :style="{ borderColor: skill.couleur, boxShadow: `0 0 15px ${skill.couleur}40` }">
              <img :src="skill.logo" :alt="`Logo ${skill.nom}`" class="skill-logo">
            </div>

            <div class="skill-texts">
              <span class="skill-name">{{ skill.nom }}</span>
              <span class="skill-level" :style="{ color: skill.couleur }">{{ skill.niveau }}</span>
            </div>

          </div>

        </div>
      </div>

    </div>
  </section>
</template>

<script setup lang="ts">
const groupedSkills = [
  {
    titre: "Actuellement concentrée sur:",
    competences: [
      { nom: "Java", niveau: "Avancé", logo: new URL('/public/img/skills/java.png', import.meta.url).href, couleur: "#f89820" },
      { nom: "SpringBoot", niveau: "Débutant", logo: new URL('/public/img/skills/springboot.png', import.meta.url).href, couleur: "#6db33f" },
      { nom: "Vue.js", niveau: "Débutant", logo: new URL('/public/img/skills/vuejs.png', import.meta.url).href, couleur: "#41b883" }
    ]
  },
  {
    titre: "Compétences confirmées :",
    competences: [
        { nom: "PostgreSQL", niveau: "Avancé", logo: new URL('/public/img/skills/postgresql.png', import.meta.url).href, couleur: "#336791" },
      { nom: "Python", niveau: "Intermédiaire", logo: new URL('/public/img/skills/python.webp', import.meta.url).href, couleur: "#3776ab" },
      { nom: "PHP", niveau: "Intermédiaire", logo: new URL('/public/img/skills/php_logo.png', import.meta.url).href, couleur: "#777bb4" },
      { nom: "Node.js", niveau: "Intermédiaire", logo: new URL('/public/img/skills/nodejs.png', import.meta.url).href, couleur: "#68a063" },
      { nom: "C", niveau: "Intermédiaire", logo: new URL('/public/img/skills/c_logo.png', import.meta.url).href, couleur: "#a8b9cc" },
      { nom: "HTML/CSS", niveau: "Avancé", logo: new URL('/public/img/skills/html.webp', import.meta.url).href, couleur: "#e34f26" }

    ]
  },
  {
    titre: "Outils & Pratiques :",
    competences: [
      { nom: "Git", niveau: "Avancé", logo: new URL('/public/img/skills/git.png', import.meta.url).href, couleur: "#f1502f" },
      { nom: "Postman", niveau: "Intermédiaire", logo: new URL('/public/img/skills/postman.webp', import.meta.url).href, couleur: "#ef5b25" }
    ]
  }
];
</script>

<style scoped>
.skills-section {
  padding: 80px 20px;
  background-color: var(--fond-page, #121212);
  color: var(--texte-principal, #ffffff);
}

.skills-header {
  text-align: center;
  margin-bottom: 60px;
}

.skills-header h2 {
  font-size: 36px;
  margin-bottom: 15px;
  color: var(--rose-dark, #c97c8a);
}

.skills-header p {
  color: var(--texte-secondaire, #a0a0a0);
  font-size: 16px;
  max-width: 600px;
  margin: 0 auto;
}

.skills-container {
  max-width: 1100px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  gap: 50px;
}

.category-title {
  font-size: 20px;
  color: var(--texte-secondaire, #a0a0a0);
  margin-bottom: 30px;
  font-weight: 500;
  border-bottom: 1px solid rgba(255,255,255,0.1); /* Ligne subtile */
  padding-bottom: 10px;
  text-align: left;
}

.skills-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 40px;
  /* Centrer les logos sur les petits écrans, les aligner à gauche sur les grands */
  justify-content: flex-start;
}

/* Comportement responsive */
@media (max-width: 768px) {
  .skills-grid {
    justify-content: center;
  }
}

.skill-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 120px;
  transition: transform 0.3s ease;
}

.skill-item:hover {
  transform: translateY(-5px);
}

/* L'anneau autour du logo inspiré de l'image 2 */
.icon-ring {
  width: 90px;
  height: 90px;
  border-radius: 50%;
  border: 4px solid transparent; /* La couleur est injectée dynamiquement par le script */
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 15px;
  background-color: rgba(255, 255, 255, 0.03); /* Léger fond pour faire ressortir le cercle */
  transition: all 0.3s ease;
}

.skill-item:hover .icon-ring {
  background-color: rgba(255, 255, 255, 0.08);
}

.skill-logo {
  width: 50px;
  height: 50px;
  object-fit: contain;
}

.skill-texts {
  text-align: center;
  display: flex;
  flex-direction: column;
  gap: 5px;
}

.skill-name {
  font-weight: 600;
  font-size: 16px;
  letter-spacing: 0.5px;
}

.skill-level {
  font-size: 13px;
  font-weight: 500;
  opacity: 0.9;
}
</style>