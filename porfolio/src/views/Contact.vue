<template>
    <section id="contact">
      <h2>Contactez-moi</h2>
      <form @submit.prevent="submitForm">
        <div class="form-group">
          <label for="name">Nom / Prénom</label>
          <input
            type="text"
            id="name"
            v-model="form.name"
            placeholder="Entrez votre nom et prénom"
            required
          />
        </div>
  
        <div class="form-group">
          <label for="subject">Objet</label>
          <input
            type="text"
            id="subject"
            v-model="form.subject"
            placeholder="Entrez l'objet de votre message"
            required
          />
        </div>
  
        <div class="form-group">
          <label for="message">Message</label>
          <textarea
            id="message"
            v-model="form.message"
            placeholder="Votre message"
            rows="5"
            required
          ></textarea>
        </div>
  
        <button type="submit">Envoyer</button>
      </form>
      <p v-if="isSubmitted" class="success-message">Message envoyé avec succès !</p>
    </section>
  </template>
  
  <script>
  export default {
    data() {
      return {
        form: {
          name: '',
          subject: '',
          message: '',
        },
        isSubmitted: false,
      };
    },
    methods: {
      submitForm() {
        // Simuler l'envoi (ou connecter à une API)
        console.log('Formulaire soumis :', this.form);
        this.isSubmitted = true;
  
        // Réinitialisation après l'envoi
        setTimeout(() => {
          this.form = { name: '', subject: '', message: '' };
          this.isSubmitted = false;
        }, 3000);
      },
    },
  };
  </script>
  
  <style scoped>
  #contact {
    padding: 2rem;
  }
  
  .form-group {
    margin-bottom: 1rem;
  }
  
  label {
    display: block;
    margin-bottom: 0.5rem;
    font-weight: bold;
  }
  
  input,
  textarea {
    width: 100%;
    padding: 0.5rem;
    border: 1px solid #ccc;
    border-radius: 4px;
  }
  
  button {
    padding: 0.75rem 1.5rem;
    background-color: #61dafb;
    border: none;
    border-radius: 4px;
    color: white;
    cursor: pointer;
    font-size: 1rem;
  }
  
  button:hover {
    background-color: #4ec0e0;
  }
  
  .success-message {
    margin-top: 1rem;
    color: green;
  }
  </style>