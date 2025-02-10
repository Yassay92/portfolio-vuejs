<template>
    <div v-if="isVisible" class="modal" @click.self="closeModal">
      <div class="modal-content">
        <button class="close" @click="closeModal">×</button>
        <h2>{{ project.title }}</h2>
        <p>Date : {{ project.date }}</p>
        <p>Technologies : {{ project.technologies }}</p>
        <a :href="project.link" target="_blank">Voir le projet</a>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: ['project', 'isVisible'],
    methods: {
      closeModal() {
        this.$emit('close');
      },
    },
  };
  </script>
  
  <style scoped>
  .modal {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.7);
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  .modal-content {
    background: white;
    padding: 2rem;
    border-radius: 8px;
    max-width: 500px;
    width: 90%;
    text-align: center;
  }
  
  .close {
    position: absolute;
    top: 10px;
    right: 10px;
    background: none;
    border: none;
    font-size: 1.5rem;
    cursor: pointer;
  }
  </style>