<script setup>
import MobileNav from './MobileNavComponent.vue'
import DesktopNav from './DesktopNavComponent.vue'
</script>

<template>
  <header class="header">
    <h1 class="header__title bold-text">Joel Chavez - Software Developer</h1>
    <!-- desktop nav -->
    <DesktopNav />
    <!-- mobile nav -->
    <MobileNav />
  </header>
</template>

<style scoped>
.header {
  background-color: #333;
  padding: 1.25rem;
  margin-bottom: 2rem;
}

.header__title {
  color: #fff;
  text-align: center;
}

/* align title and mobile nav horizontally */
@media (max-width: 768px) {
  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
}
</style>
