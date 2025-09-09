<script setup>
const items = [{ name: "Sobre mí", href: "#about" }, { name: "Proyectos", href: "#projects" }, { name: "Experiencia", href: "#experience" }, { name: "Estudios", href: "#education" }, { name: "Contacto", href: "#contact" }]
</script>

<template>
  <nav class="desktop-nav">
    <ul class="desktop-nav__list light-text">
      <li class="desktop-nav__item" v-for="item in items" :key="item.href">
        <a class="desktop-nav__link" :href="item.href">{{ item.name }}</a>
      </li>
    </ul>
  </nav>
</template>

<style scoped>
/* hide desktop nav on screens smaller than 768px */
.desktop-nav {
  display: none;
}

.desktop-nav__list {
  list-style: none;
  background-color: #333;
  display: flex;
  justify-content: center;
}

.desktop-nav__item {
  display: inline-block;
  margin-right: 0.6rem;
  padding: 0.6rem;
  font-size: 1rem;
}

.desktop-nav__link {
  color: #fff;
  text-decoration: none;
  padding: 0.6rem;

  &:hover {
    background-color: #666;
    color: #fff;
  }
}

/* show desktop nav on screens larger than 768px */
@media (min-width: 768px) {
  .desktop-nav {
    display: block;
  }
}
</style>
