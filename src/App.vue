<script setup>
import NavBar from './components/NavBar.vue';
import Banner from './components/Banner.vue';
import Education from './components/education.vue';
import Skill from './components/Skill.vue';
import Project from './components/Project.vue';
</script>

<template>
  <header class="header">
    <!-- Barra de nevegación -->
    <NavBar />
  </header>
  <!-- contenido principal -->
  <main>
    <!-- componente banner -->
    <div id="inicio">

      <Banner/>
    </div>
    <!-- componente educación -->
    <div id="educacion">
      <education/>
    </div>
    <!-- componente habilidades -->
    <div id="habilidades">
      <Skill/>
    </div>
    <!-- componente  -->
    <div id="proyectos">
      <Project/>
    </div>
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
