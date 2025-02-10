<template>
    <footer>
      <p>&copy; {{ new Date().getFullYear() }} - Dernière mise à jour : {{ lastUpdated }}</p>
      <ul>
        <li><a href="https://github.com" target="_blank">GitHub</a></li>
        <li><a href="https://linkedin.com" target="_blank">LinkedIn</a></li>
      </ul>
    </footer>
  </template>
  
  <script>
  export default {
    data() {
      return {
        lastUpdated: '01 février 2025',
      };
    },
  };
  </script>
  
  <style scoped>
  footer {
    text-align: center;
    padding: 1rem;
    background-color: #222;
    color: white;
  }
  
  footer ul {
    list-style: none;
    display: flex;
    justify-content: center;
    gap: 1rem;
    padding: 0;
  }
  
  footer a {
    color: #61dafb;
    text-decoration: none;
  }
  </style>