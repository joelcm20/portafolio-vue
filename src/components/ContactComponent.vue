<template>
  <section class="contact container" id="contact">
    <article class="form-container">
      <!-- <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSfFGJzyOlyYHALyYGSsFr0Y09qShvvXtDtSX3iwqkpEvmOMLQ/viewform?embedded=true"
        width="100%" loading="lazy" allowfullscreen referrerpolicy="no-referrer">Cargando…</iframe> -->
        <iframe src="https://docs.google.com/forms/d/e/1FAIpQLSfFGJzyOlyYHALyYGSsFr0Y09qShvvXtDtSX3iwqkpEvmOMLQ/viewform?embedded=true" width="640" height="792" frameborder="0" marginheight="0" marginwidth="0">Cargando…</iframe>
    </article>
  </section>
</template>

<style scoped>
.form-container {
  display: flex;
  justify-content: center;
  padding: 1rem;
}

.form-container iframe {
  width: 600px;
  height: 950px;
  border: none;
}

@media (min-width: 768px) {
  .form-container {
    padding: 0;
  }
}
</style>
