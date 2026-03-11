<template>
  <section id="contact" class="contact-section">
    <h2>Travaillons ensemble</h2>

    <p class="contact-text">
      Une question, une proposition ou simplement envie de discuter code ? <br>
      Remplissez ce formulaire et je vous répondrai dans les plus brefs délais.
    </p>

    <form @submit.prevent="envoyerMessage" class="contact-form">

      <div class="form-group">
        <label for="nom">Nom ou Entreprise</label>
        <input
            type="text"
            id="nom"
            v-model="form.nom"
            name="Nom"
            placeholder="Ex: Jane Doe"
            required
        >
      </div>

      <div class="form-group">
        <label for="email">Adresse e-mail</label>
        <input
            type="email"
            id="email"
            v-model="form.email"
            name="Email"
            placeholder="Ex: jane@entreprise.com"
            required
        >
      </div>

      <div class="form-group">
        <label for="message">Votre message</label>
        <textarea
            id="message"
            v-model="form.message"
            name="Message"
            rows="5"
            placeholder="Bonjour Charlotte, j'aimerais vous parler de..."
            required
        ></textarea>
      </div>

      <p v-if="statut === 'succes'" class="msg-succes">Message envoyé avec succès ! Je vous réponds vite.</p>
      <p v-if="statut === 'erreur'" class="msg-erreur">Oups, une erreur s'est produite. Veuillez réessayer.</p>

      <button type="submit" class="btn-submit" :disabled="statut === 'en_cours'">
        {{ statut === 'en_cours' ? 'Envoi...' : 'Envoyer le message ' }}
      </button>

    </form>

    <div class="social-links">
      <a href="https://linkedin.com/in/votre-profil" target="_blank" class="social-btn">
        💼 LinkedIn
      </a>
      <a href="https://github.com/votre-pseudo" target="_blank" class="social-btn">
        💻 GitHub
      </a>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const form = ref({
  nom: '',
  email: '',
  message: ''
})

const statut = ref('attente')

const envoyerMessage = async () => {
  statut.value = 'en_cours'

  try {
    const response = await fetch("https://formspree.io/f/xwvrlqve", {
      method: "POST",
      headers: {
        "Content-Type": "application/json",
        "Accept": "application/json"
      },
      body: JSON.stringify({
        Nom: form.value.nom,
        Email: form.value.email,
        Message: form.value.message
      })
    })

    if (response.ok) {
      statut.value = 'succes'
      form.value = { nom: '', email: '', message: '' }

      setTimeout(() => { statut.value = 'attente' }, 5000)
    } else {
      statut.value = 'erreur'
    }
  } catch (error) {
    statut.value = 'erreur'
  }
}
</script>

<style scoped>

.msg-succes {
  color: #2e7d32;
  background-color: #edf7ed;
  padding: 10px;
  border-radius: 8px;
  font-size: 14px;
  margin-bottom: 20px;
  text-align: center;
}

.msg-erreur {
  color: #d32f2f;
  background-color: #fdeded;
  padding: 10px;
  border-radius: 8px;
  font-size: 14px;
  margin-bottom: 20px;
  text-align: center;
}


.btn-submit:disabled {
  opacity: 0.7;
  cursor: not-allowed;
}

.contact-section {
  padding: 100px 20px;
  background-color: var(--fond-page);
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.contact-section h2 {
  color: var(--rose-dark);
  font-size: 32px;
  margin-bottom: 20px;
}

.contact-text {
  color: var(--texte-secondaire);
  font-size: 18px;
  line-height: 1.6;
  max-width: 600px;
  margin-bottom: 40px;
}

.contact-form {
  background: var(--fond-element);
  padding: 40px;
  border-radius: 12px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
  width: 100%;
  max-width: 500px;
  text-align: left;
  margin-bottom: 50px;
}

.form-group {
  margin-bottom: 25px;
  display: flex;
  flex-direction: column;
}

.form-group label {
  font-size: 14px;
  font-weight: 600;
  color: var(--texte-principal);
  margin-bottom: 8px;
}

.form-group input,
.form-group textarea {
  padding: 12px 15px;
  border: 1px solid #ddd;
  border-radius: 8px;
  font-family: inherit;
  font-size: 15px;
  color: var(--texte-principal);
  background-color: #fafafa;
  transition: all 0.3s ease;
}

.form-group input:focus,
.form-group textarea:focus {
  outline: none;
  border-color: var(--rose);
  background-color: white;
  box-shadow: 0 0 0 3px rgba(232, 160, 173, 0.2);
}

.btn-submit {
  width: 100%;
  padding: 15px;
  background-color: var(--rose);
  color: white;
  border: none;
  border-radius: 8px;
  font-weight: 600;
  font-size: 16px;
  cursor: pointer;
  transition: all 0.3s ease;
}

.btn-submit:hover:not(:disabled) {
  background-color: var(--rose-dark);
  transform: translateY(-2px);
}

.social-links {
  display: flex;
  gap: 20px;
  flex-wrap: wrap;
  justify-content: center;
}

.social-btn {
  display: flex;
  align-items: center;
  gap: 8px;
  padding: 10px 20px;
  background-color: var(--fond-element);
  color: var(--texte-principal);
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  text-decoration: none;
  font-weight: 500;
  transition: all 0.2s ease;
}

.social-btn:hover {
  border-color: var(--rose);
  color: var(--rose-dark);
  transform: scale(1.05);
}
</style>