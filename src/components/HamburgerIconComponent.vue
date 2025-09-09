<script setup>
defineProps({ isOpen: Boolean });
</script>

<template>
  <div class="icon" :class="{ animation: isOpen }">
    <div></div>
    <div></div>
    <div></div>
  </div>
</template>

<style scoped>
.icon>div {
  position: absolute;
  transition: all 0.2s ease;
  width: 100%;
  height: 0.2rem;
  background-color: #fff;
  left: 0;
}

.icon>div:first-child {
  top: 0.5rem;
}

.icon>div:nth-child(2) {
  top: 1rem;
}

.icon>div:last-child {
  top: 1.5rem;
}

/* icon animation  */
.animation>div:first-child {
  transform: rotate(45deg);
  top: 0.5rem;
}

.animation>div:nth-child(2) {
  opacity: 0;
}

.animation>div:last-child {
  transform: rotate(-45deg);
  top: 0.5rem;
}
</style>
