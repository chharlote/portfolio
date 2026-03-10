<template>
  <section class="hero">
    <div class="hero-text">
      <h1>Bonjour, moi c'est Charlotte 👋</h1>

      <p>
        Je suis passionnée par l'informatique et le développement.
        J'aime créer des projets web, apprendre de nouvelles technologies
        et transformer des idées en applications concrètes.
      </p>

      <p>
        Sur ce portfolio vous pourrez découvrir mes projets,
        les technologies que j'utilise et mon parcours.
      </p>

      <router-link to="/projects" class="btn">
        Voir mes projets
      </router-link>
    </div>

    <div class="hero-image">
      <img src="../assets/img/profile.png" alt="photo profil">
    </div>
  </section>
</template>

<style scoped>
.hero {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 80px;
}

.hero-text {
  max-width: 500px;
}

.hero h1 {
  font-size: 42px;
  margin-bottom: 20px;
  color: #c97c8a;
}

.hero p {
  margin-bottom: 15px;
  color: #555;
}

.btn {
  display: inline-block;
  margin-top: 15px;
  padding: 12px 22px;
  background: #e8a0ad;
  color: white;
  border-radius: 8px;
  text-decoration: none;
}

.btn:hover {
  background: #d88c99;
}

.hero-image img {
  width: 300px;
  border-radius: 20px;
}
</style>