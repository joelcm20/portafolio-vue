<script setup>
defineProps({ title: String, description: String, image: String, link: String })
</script>

<template>
  <article class="card">
    <img class="card__img" :src="image" alt="Proyecto 1">
    <div class="card__content">
      <h3 class="card__title">{{ title }}</h3>
      <p class="card__description">{{ description }}</p>
      <a class="card__link" :href="link">Ver proyecto</a>
    </div>
  </article>
</template>

<style scoped>
.card {
  background-color: #fff;
  border-radius: 0.75rem;
  overflow: hidden;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

.card__img {
  width: 100%;
  height: auto;
  display: block;
}

.card__content {
  padding: 1rem;
}

.card__title {
  margin-top: 0;
  font-size: 1.25rem;
  margin-bottom: 0.5rem;
}

.card__description {
  margin-bottom: 1rem;
  color: #555;
}

.card__link {
  text-decoration: none;
  color: #007bff;
  font-weight: bold;
  transition: color 0.3s;
}

.card__link:hover {
  color: #0056b3;
}

@media (min-width: 768px) {
  .card {
    flex: 1 1 calc(50% - 2rem);
    max-width: calc(50% - 2rem);
  }
}

@media (min-width: 1024px) {
  .card {
    flex: 1 1 calc(33.333% - 2rem);
    max-width: calc(33.333% - 2rem);
  }
}
</style>
