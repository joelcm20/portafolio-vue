<script setup>
import HeaderComponent from './components/HeaderComponent.vue'
import AboutMeComponent from './components/AboutMeComponent.vue'
import ProjectsComponent from './components/ProjectsComponent.vue'
import ExperienceComponent from './components/ExperienceComponent.vue'
import EducationComponent from './components/EducationComponent.vue'
import ContactComponent from './components/ContactComponent.vue'
import FooterComponent from './components/FooterComponent.vue'

const goToTop = () => {
  window.scrollTo({
    top: 0,
    behavior: 'smooth'
  })
}
</script>

<template>
  <div>
    <HeaderComponent />
    <AboutMeComponent />
    <ProjectsComponent />
    <ExperienceComponent />
    <EducationComponent />
    <ContactComponent />
    <FooterComponent />

    <!-- scroll to top -->
    <span class="scroll-to-top" v-on:click="goToTop" >&#8593;</span>
  </div>
</template>

<style scoped>
.scroll-to-top {
  position: fixed;
  bottom: 20px;
  right: 20px;
  width: 40px;
  height: 40px;
  background-color: #333;
  color: #fff;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 24px;
  cursor: pointer;
  z-index: 9999;
}
</style>
