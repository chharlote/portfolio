<template>
  <nav class="navbar">
    <h1 class="logo">Charlotte</h1>

    <div class="links">
      <router-link to="/">Accueil</router-link>
      <router-link to="/projects">Projets</router-link>
    </div>
  </nav>
</template>

<style scoped>
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 25px 60px;
  background: #fff7f9;
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