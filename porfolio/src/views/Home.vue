<template>
    <div>
      <section id="presentation">
        <h1>Bienvenue sur mon Portfolio</h1>
        <p>Je suis [Yacine Frikh], développeur web spécialisé en Vue.js.</p>
      </section>
  
      <section id="creations">
        <h2>Mes Créations</h2>
        <div class="projects">
          <ProjectCard
            v-for="project in projects"
            :key="project.id"
            :project="project"
            @open-modal="openModal"
          />
        </div>
      </section>
  
      <Modal :project="selectedProject" :isVisible="isModalVisible" @close="closeModal" />
    </div>
  </template>
  
  <script>
  import ProjectCard from '@/components/ProjectCard.vue';
  import Modal from '@/components/Modal.vue';
  
  export default {
    components: { ProjectCard, Modal },
    data() {
      return {
        projects: [
          { id: 1, title: 'Projet 1', image: '@/assets/images/project1.jpg', date: '2023', technologies: 'Vue.js, CSS', link: '#' },
          { id: 2, title: 'Projet 2', image: '@/assets/images/project2.jpg', date: '2024', technologies: 'HTML, CSS', link: '#' },
        ],
        selectedProject: null,
        isModalVisible: false,
      };
    },
    methods: {
      openModal(project) {
        this.selectedProject = project;
        this.isModalVisible = true;
      },
      closeModal() {
        this.isModalVisible = false;
        this.selectedProject = null;
      },
    },
  };
  </script>
  
  <style>
  .projects {
    display: flex;
    gap: 1rem;
  }
  </style>