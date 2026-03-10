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
  /*background: var(--fond);*/
  background: var(--fond-element);
  width: 100%;
  box-sizing: border-box;


  box-shadow: 0 4px 15px rgba(201, 124, 138, 0.15);

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