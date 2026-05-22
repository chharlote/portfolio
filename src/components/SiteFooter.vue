<template>
  <footer class="footer">
    <div class="footer-content">
      <p>© {{ currentYear }} Charlotte. Tous droits réservés.</p>
      <p class="made-with">
        Développé avec ❤️ et <a href="https://vuejs.org/" target="_blank">Vue.js</a>
      </p>
    </div>
  </footer>
</template>

<script setup>
import { computed } from 'vue'

const currentYear = computed(() => new Date().getFullYear())
</script>

<style scoped>
.footer {
  background-color: var(--fond-element);
  padding: 30px 20px;
  text-align: center;
  border-top: 1px solid #eaeaea;
}

.footer-content {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.footer p {
  color: var(--texte-secondaire);
  font-size: 14px;
  margin: 0;
}

.made-with a {
  color: var(--rose-dark);
  text-decoration: none;
  font-weight: 600;
  transition: color 0.2s ease;
}

.made-with a:hover {
  color: var(--rose);
  text-decoration: underline;
}
</style>