<script setup>
import CardProject from './CardProjectComponent.vue';

const projects = [{
  id: 1,
  title: "Portafolio Personal",
  description: "Un sitio web personal para mostrar mis trabajos y habilidades como desarrollador frontend.",
  image: "/images/portafolio.png", link: "#"
}, {
  id: 2,
  title: "Gestor de Tareas",
  description: "Una aplicación web para crear, editar y gestionar tareas diarias con autenticación.",
  image: "/images/api-user-gestion.png",
  link: "#"
}, {
  id: 3,
  title: "API REST para Gestión de Usuarios",
  description: "Una API desarrollada con Spring Boot y PostgreSQL, que permite registrar, autenticar y administrar usuarios desde aplicaciones frontend.",
  image: "/images/todo-list.png",
  link: "#"
}]
</script>

<template>
  <section class="my-projects container" id="projects">
    <h2 class="my-projects__title">Mis Proyectos</h2>
    <div class="my-projects__cards">
      <CardProject v-for="project in projects" :title="project.title" :description="project.description"
        :image="project.image" :link="project.link" :key="project.id" />
    </div>
  </section>
</template>


<style scoped>
.my-projects {
  padding: 2rem 1rem;
}

.my-projects__title {
  text-align: center;
  margin-bottom: 2rem;
  font-size: 2rem;
}

.my-projects__cards {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

@media (min-width: 768px) {
  .my-projects__cards {
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
  }
}
</style>
