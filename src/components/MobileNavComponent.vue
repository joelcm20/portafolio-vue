<script setup>
import HamburgerIcon from "./HamburgerIconComponent.vue";
import { ref, onMounted, onBeforeMount } from "vue";

const isMenuOpen = ref(false);
const menuRef = ref(null);
const items = [{ name: "Sobre mí", href: "#about" }, { name: "Proyectos", href: "#projects" }, { name: "Experiencia", href: "#experience" }, { name: "Estudios", href: "#education" }, { name: "Contacto", href: "#contact" }]

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};

const handleClickOutside = (e) => {
  // close menu if clicked outside
  if (isMenuOpen.value && menuRef.value && menuRef.value && !menuRef.value.contains(e.target)) {
    isMenuOpen.value = false;
  }
};

onMounted(() => {
  document.addEventListener("click", handleClickOutside);
});

onBeforeMount(() => {
  document.removeEventListener("click", handleClickOutside);
});
</script>

<template>
  <nav class="mobile-nav" ref="menuRef">
    <HamburgerIcon :isOpen="isMenuOpen" @click="toggleMenu" class="mobile-nav__icon"
      :class="{ animation: isMenuOpen }" />
    <ul class="mobile-nav__list" :class="{ 'display-block': isMenuOpen }">
      <li class="mobile-nav__item" v-for="item in items" :key="item.href">
        <a class="mobile-nav__link" :href="item.href">{{ item.name }}</a>
      </li>
    </ul>
  </nav>
</template>

<style scoped>
/* por defecto, en tamaño mobile se muestra el nav mobile */
.mobile-nav {
  margin-top: 0.6rem;
  display: flex;
  justify-content: center;
  position: relative;
}

.mobile-nav__list {
  display: none;
  text-align: center;
  list-style: none;
  background-color: #333;
  border: 1px solid #f5f5f5;
  margin-top: 2rem;
  padding: 0.5rem;
  border-radius: 0.5rem;
  position: absolute;
  top: 0.5rem;
  right: 0;
}

.mobile-nav__icon {
  cursor: pointer;
  margin: 0.5rem;
  position: relative;
  width: 1.5rem;
  height: 1.5rem;
}

.mobile-nav__item {
  width: 100%;
  font-size: 1rem;
}

.mobile-nav__link {
  display: inline-block;
  width: 100%;
  color: #fff;
  text-decoration: none;
  padding: 0.6rem;

  &:hover {
    background-color: #666;
    color: #fff;
  }
}

.display-block {
  display: block;
}

/* desktop style */
@media (min-width: 768px) {
  .mobile-nav {
    display: none;
  }
}
</style>
