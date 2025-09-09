<script setup>
const items = [{ id: 1, title: "Universidad Tecnológica Nacional", diration: "Marzo 2025 - Presente" }]
</script>

<template>
  <section class="timeline" id="education">
    <div class="container">
      <h2>Mis Estudios</h2>

      <div class="timeline-item" v-for="item in items" :key="item.id">
        <h3>{{ item.title }}</h3>
        <div class="duration">{{ item.diration }}</div>
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
