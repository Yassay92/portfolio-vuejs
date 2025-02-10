<template>
    <div class="project-card" @click="openModal">
      <img :src="project.image" :alt="project.title">
      <h3>{{ project.title }}</h3>
    </div>
  </template>
  
  <script>
  export default {
    props: ['project'],
    methods: {
      openModal() {
        this.$emit('open-modal', this.project);
      }
    }
  };
  </script>