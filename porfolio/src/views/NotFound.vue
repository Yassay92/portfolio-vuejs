<template>
    <div class="not-found">
      <h1>404</h1>
      <p>Oups ! La page que vous recherchez n'existe pas.</p>
      <router-link to="/">Retour à l'accueil</router-link>
    </div>
  </template>
  
  <script>
  export default {};
  </script>
  
  <style scoped>
  .not-found {
    text-align: center;
    margin-top: 5rem;
  }
  
  h1 {
    font-size: 5rem;
    color: #ff6b6b;
  }
  
  p {
    font-size: 1.25rem;
    margin: 1rem 0;
  }
  
  a {
    text-decoration: none;
    color: #61dafb;
    font-size: 1rem;
    border: 1px solid #61dafb;
    padding: 0.5rem 1rem;
    border-radius: 4px;
    transition: background-color 0.3s, color 0.3s;
  }
  
  a:hover {
    background-color: #61dafb;
    color: white;
  }
  </style>