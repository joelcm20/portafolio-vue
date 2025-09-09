<script setup>
const items = [
  {
    id: 1,
    name: "Desarrollador Backend – DataSolutions",
    duration: "Enero 2023 - Presente",
    description: "Encargado del desarrollo de APIs REST con Spring Boot y FastAPI. Integración de bases de datos relacionales y no relacionales como PostgreSQL y MongoDB. Implementación de pruebas automatizadas y despliegue continuo."
  },
  {
    id: 2,
    name: "Asistente de Desarrollo Web – CodeLabs", duration: "Marzo 2021 - Diciembre 2022", description: "Colaboración en proyectos internos. Apoyo en mantenimiento de sitios con HTML, CSS y JavaScript."
  },
  {
    id: 3, name: "Prácticas Profesionales – WebNova Studio", duration: "Agosto 2020 - Febrero 2021", description: "Diseño de sitios básicos y carga de contenido. Aprendizaje en CMS como WordPress."
  }
]
</script>

<template>
  <section class="timeline" id="experience">
    <div class="container">
      <h2>Mi Experiencia</h2>
      <div class="timeline-item" v-for="item in items" :key="item.id">
        <h3>{{ item.name }}</h3>
        <div class="duration">{{ item.duration }}</div>
        <p>{{ item.description }}</p>
      </div>
    </div>
  </section>
</template>


<style scoped>
section.timeline {
  max-width: 800px;
  margin-right: auto;
  margin-left: auto;
}

section.timeline h2 {
  text-align: center;
  margin-bottom: 2rem;
  font-size: 2rem;
  /* color: #333; */
}

.timeline-item {
  position: relative;
  padding-left: 40px;
  margin-bottom: 2rem;
  border-left: 3px solid #ccc;
}

.timeline-item::before {
  content: '';
  position: absolute;
  left: -8px;
  top: 0;
  width: 16px;
  height: 16px;
  background-color: #555;
  border: 2px solid white;
  border-radius: 50%;
  box-shadow: 0 0 0 2px #555
}

.timeline-item h3 {
  margin: 0;
  font-size: 1.2rem;
  color: #333;
}

.timeline-item .duration {
  font-size: 0.9rem;
  color: #555;
  margin-bottom: 0.5rem;
}

.timeline-item p {
  margin: 0.5rem 0 0;
  color: #333;
}
</style>
