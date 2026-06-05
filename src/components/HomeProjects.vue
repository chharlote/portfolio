<template>
  <section id="projets" class="home-projects">
    <h2>Mes Projets</h2>
    <p class="intro-text">Voici une sélection de mes réalisations les plus significatives.</p>

    <div class="projects-grid">

      <div class="project-card" v-for="(projet, index) in projets" :key="index">

        <div class="img-placeholder">
          <img :src="projet.image" :alt="projet.imageAlt">
        </div>

        <div class="project-techs">
          <span class="tech-mini-badge" v-for="tech in projet.technologies" :key="tech">
            {{ tech }}
          </span>
        </div>

        <h3>{{ projet.titre }}</h3>
        <h4 v-if="projet.sousTitre">{{ projet.sousTitre }}</h4>

        <div class="project-meta">
          <span class="meta-item" v-if="projet.duree">
            ⏱️ {{ projet.duree }}
          </span>
          <span class="meta-item" v-if="projet.equipe">
            👥 {{ projet.equipe }} {{ projet.equipe > 1 ? 'personnes' : 'personne' }}
          </span>
        </div>

        <p>
          <template v-for="(point, i) in projet.description" :key="i">
            ▸ {{ point }}<br>
          </template>
        </p>

        <a v-if="projet.lien" :href="projet.lien" target="_blank" class="btn-projet">
          Voir le code
        </a>

      </div>

    </div>
  </section>
</template>

<script setup lang="ts">
const projets = [
  {
    titre: "BioEchec VR",
    sousTitre: null,
    image: new URL('../assets/img/jeurv.png', import.meta.url).href,
    imageAlt: "BioEchec VR",
    technologies: ["Unreal Engine 5", "Blueprint"],
    duree: "1 semaine",
    equipe: 6,
    description: [
      "Réflexion autour du gameplay en groupe",
      "Création du jeu VR autour d'un thème de laboratoire scientifique",
      "Implémentation complète d'un environnement VR immersif avec mécaniques de jeu",
      "Mécanique de jeu réalisée en blueprint"
    ],
    lien: null
  },
  {
    titre: "Skyrift",
    sousTitre: "Jeu tour par tour sur le thème des dragons",
    image: new URL('../assets/img/skyrift.png', import.meta.url).href,
    imageAlt: "Skyrift",
    technologies: ["Python", "Pygame", "GitHub", "Trello"],
    duree: "3 mois",
    equipe: 5,
    description: [
      "Création d'un Game Design et Technical Design",
      "Implémentation du moteur de jeu avec Pygame",
      "Création d'une IA complète en tant que joueur",
      "Équilibrage du gameplay, optimisation de l'IA pour fluidifier le jeu",
      "Mise en place d'un suivi de projet avec Trello"
    ],
    lien: "https://github.com/chharlote/skyrift"
  },
  {
    titre: "API Tennis",
    sousTitre: null,
    image: new URL('../assets/img/swagger-tennis.png', import.meta.url).href,
    imageAlt: "API Tennis",
    technologies: ["Node.js", "TypeScript", "PostgreSQL", "Prisma"],
    duree: "2 jours",
    equipe: 1,
    description: [
      "Élaboration de l’API en Node.js",
      "Création de tests d’intégration avec POSTMAN",
      "Réalisation de la documentation avec Swagger",
      "Création de la base de données PostgreSQL à laquelle fait appel l’API"
    ],
    lien: "https://github.com/chharlote/api_tennis"
  },
  {
    titre: "OceanMan",
    sousTitre: "Nuit de l'info 2024",
    image: new URL('../assets/img/nuitinfo.png', import.meta.url).href,
    imageAlt: "OceanMan",
    technologies: ["PHP", "HTML", "CSS"],
    duree: "1 nuit",
    equipe: 5,
    description: [
      "Création d'un site web interactif sur le thème de la pollution des océans",
      "Conception du site web en une nuit",
      "Site cliquable afin de voir une similitude entre une maladie humaine et les conséquences de la pollution marine"
    ],
    lien: "https://github.com/chharlote/oceanman"
  },
  {
    titre: "Création d'un CRUD complet",
    sousTitre: "(Mission d'alternance)",
    image: new URL('../assets/img/crud.jpg', import.meta.url).href,
    imageAlt: "CRUD Java",
    technologies: ["Java", "SpringBoot", "Junit", "Postman"],
    duree: "1 semaine",
    equipe: 1,
    description: [
      "Réalisation du CRUD en JAVA SpringBoot suite à un besoin client",
      "Élaboration des tests unitaires avec Junit et des tests d’intégration avec Postman",
      "Respect des conventions de développement pour la qualité de code"
    ],
    lien: null
  },
  {
    titre: "Création d’un site web en PHP",
    sousTitre: null,
    image: new URL('../assets/img/php.png', import.meta.url).href,
    imageAlt: "Gestion PHP",
    technologies: ["PHP", "PosgreSQL"],
    duree: "1 semaine",
    equipe: 1,
    description: [
      "Site pour la gestion de cours, comprend des étudiants, des enseignants et des cours et des matières",
      "Conception de la base de données complète en PostgreSQL",
      "Mise en place de routines et fonctions en PL/pgSQL",
        "Liaison de la base de données au site en PHP"
    ],
    lien: "https://github.com/chharlote/gestion-cours-pgsql/tree/main"
  },
  {
    titre: "Application de gestion d'image astronomique",
    sousTitre: null,
    image: new URL('../assets/img/astro_sae.png', import.meta.url).href,
    imageAlt: "SAE Astro",
    technologies: ["Python", "Skyview"],
    duree: "1 semaine",
    equipe: 2,
    description: [
      "Mise en place d'outils infrarouge et de filter de couleur",
      "Découverte et utilisation des fichiers d’images astronomiques (FIT et FITS)",
      "Analyse de fichier et données d'images astronomique"
    ],
    lien: "https://github.com/chharlote/astro-image-viewer"
  }
];
</script>

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
  margin-bottom: 10px;
}

.project-card h4 {
  color: var(--rose);
  font-size: 16px;
  margin-top: 0;
  margin-bottom: 15px;
  font-weight: 500;
}


.project-meta {
  display: flex;
  justify-content: center;
  gap: 20px;
  width: 100%;
  margin-bottom: 20px;
  padding-bottom: 15px;
  border-bottom: 1px solid rgba(0, 0, 0, 0.05);
}

.meta-item {
  display: flex;
  align-items: center;
  gap: 6px;
  font-size: 14px;
  color: var(--texte-secondaire);
  font-weight: 500;
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
  margin-top: auto;
}

.btn-projet:hover {
  background-color: var(--rose);
  color: white;
}
</style>