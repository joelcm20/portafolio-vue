<script setup>
// get current year
const currentYear = new Date().getFullYear();
</script>

<template>
  <footer class="footer container">
    <div class="footer-container">
      <p>&copy; {{ currentYear }} Joel Chavez. Todos los derechos reservados.</p>
      <a href="https://github.com/joelcm20" target="_blank" aria-label="GitHub">
        <svg class="github-icon" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
          <path
            d="M12 .297a12 12 0 00-3.8 23.4c.6.1.8-.3.8-.6v-2.3c-3.3.7-4-1.6-4-1.6-.6-1.5-1.4-1.9-1.4-1.9-1.1-.8.1-.8.1-.8 1.2.1 1.8 1.2 1.8 1.2 1.1 1.9 2.9 1.4 3.6 1.1.1-.8.4-1.4.7-1.7-2.6-.3-5.4-1.3-5.4-5.9 0-1.3.5-2.4 1.2-3.3-.1-.3-.5-1.5.1-3.2 0 0 1-.3 3.3 1.2a11.3 11.3 0 016 0c2.2-1.5 3.3-1.2 3.3-1.2.6 1.7.2 2.9.1 3.2.8.9 1.2 2 1.2 3.3 0 4.6-2.8 5.6-5.5 5.9.4.3.7.9.7 1.9v2.8c0 .3.2.7.8.6A12 12 0 0012 .297z" />
        </svg>
      </a>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  background-color: #f8f9fa;
  padding: 2rem 1rem;
  font-size: 0.95rem;
  color: #333;
  text-align: center;
}

.footer-container {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
}

.footer a {
  color: #007bff;
  text-decoration: none;
  transition: color 0.3s;
}

.footer a:hover {
  color: #0056b3;
}

.github-icon {
  width: 24px;
  height: 24px;
  display: inline-block;
}
</style>
