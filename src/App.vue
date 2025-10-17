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

.banner {
  position: relative;
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  gap: 2rem;
  min-height: calc(100vh - 6.5rem);
}

.banner__img img {
  height: 40rem;
  width: 40rem;
  border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%;
}

.banner__content {
  flex: 1 1 35rem;
}

.banner__content .content__title {
  font-size: 4rem;
  color: var(--title-color);
  margin-bottom: 2rem;
}

.banner__content .content__sub-title {
  font-size: 3rem;
  color: var(--text-color);
  padding: .5rem 0;
  display: block;
}

.banner__content .content__description {
  font-size: 1.5rem;
  color: var(--text-color);
  padding: 1rem 0;
}

@media (max-width: 500px) {
  .banner {
    padding-top: 9rem;
    /* display: block; */
  }

  .banner__img img {
    margin-bottom: -50px;
    height: 35rem;
    width: 35rem;

  }

  .banner__content {
    margin-bottom: 10rem;
  }
}

</style>
