<template>
    <header>
      <img src="@/assets/favicon.png" alt="Logo" class="logo" @click="scrollToTop" />
      <nav>
        <ul>
          <li><a href="#presentation">Présentation</a></li>
          <li><a href="#creations">Créations</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
    </header>
  </template>
  
  <script>
  export default {
    methods: {
      scrollToTop() {
        window.scrollTo({ top: 0, behavior: 'smooth' });
      },
    },
  };
  </script>
  
  <style scoped>
  header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem;
    background-color: #333;
    color: white;
  }
  
  .logo {
    width: 50px;
    cursor: pointer;
  }
  
  nav ul {
    list-style: none;
    display: flex;
    gap: 1rem;
  }
  
  nav a {
    color: white;
    text-decoration: none;
  }
  </style>