<script setup>
import NavBar from './components/NavBar.vue';
import Banner from './components/Banner.vue';
</script>

<template>
  <header class="header">
    <!-- Barra de nevegación -->
    <NavBar />
  </header>
  <!-- contenido principal -->
  <main>
    <Banner/>
  </main>
</template>

<style scoped>
.header {
  width: 100%;
  display: flex;
  justify-content: center;
  padding: 2em;
  position: fixed;
  z-index: 1000;
  background: var(--color-background);
  opacity: 0.9;
}



</style>
