<template>
  <nav class="navbar">
    <h1 class="logo">Charlotte</h1>

    <div class="links">
      <a href="#accueil">Accueil</a>
      <a href="#projets">Projets</a>
      <a href="#parcours">Parcours</a>
      <a href="#competences">Compétences</a>
      <a href="#contact">Contact</a>

    </div>
  </nav>
</template>
<style scoped>
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 25px 60px;
  /*background: var(--fond);*/
  background: var(--fond-element);
  width: 100%;
  box-sizing: border-box;


  box-shadow: 0 4px 15px rgba(201, 124, 138, 0.15);
  position: sticky;
  top: 0;
  z-index: 1000;

}

.logo {
  font-weight: bold;
  font-size: 22px;
  color: #c97c8a;
}

.links a {
  margin-left: 25px;
  text-decoration: none;
  color: #e8a0ad !important;
  font-weight: 500;
}

.links a:hover {
  color: var(--rose-dark);
}


</style>
<script setup lang="ts">
</script>