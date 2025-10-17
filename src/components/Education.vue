<script setup>
import { ref } from 'vue';
const education = ref([
  {
    title: '2025',
    detailShort: 'Técnicatura Universitaria en Programación',
    detail: `En el presente año inicio mis estudios en la TUP, Facultad Regional San Rafael`
  },
  {
    title: '2023',
    detailShort: 'Argentina Programa',
    detail: `Realicé los cursos de Argentina Programa, primera y segunda etapa`
  },
  {
    title: '2011',
    detailShort: 'Técnico Universitario en Informática',
    detail: `Culminos mis estudios egresandome como TUI, en la UNLaR Sede Villa Unión`
  }
]);
</script>

<template>
  <section id="education" class="education">
    <h1 class="section_title">Educación</h1>

    <div class="education__container">

      <div v-for="educ in education" class="card">
        <div class="card-body">
          <h1 class="card-title">{{ educ.title }}</h1>
          <p class="card--detail_short">{{ educ.detailShort }}</p>
          <p class="card--detail">{{ educ.detail }}</p>
        </div>
      </div>

    </div>

  </section>
</template>

<style scoped>
/* educación */
.education .education__container {
  display: relative;
  margin: 4rem auto;
  /* overflow: hidden; */
}

.card {
  width: 45%;
  padding: 30px;
  border-radius: 10px;
  color: var(--title-color);
  display: block;
  margin: 10rem 0;
  position: relative;
}

.card__model {
  position: relative;
  display: block;
  max-width: 150px;
  height: 200px;
  padding: 5px;
  border-radius: 10px;
  color: var(--title-color);

}

.card__model .card__model--detail {
  max-height: 110px;
  text-overflow: ellipsis;
  overflow: hidden;
}

.card:nth-child(even) {
  margin-left: auto;
}

.card:nth-child(even):before {
  content: '';
  position: absolute;
  left: -15%;
  top: 50%;
  transform: translateY(-50%);
  width: 20px;
  height: 20px;
  border: 5px solid #191919;
  border-radius: 50%;
}

.card:nth-child(even):after {
  content: '';
  position: absolute;
  left: -8.5%;
  top: 50%;
  transform: translateY(-50%);
  width: 7%;
  height: 2px;
  background: #fff;
  z-index: -1;
}

.card:nth-child(odd):before {
  content: '';
  position: absolute;
  right: -13%;
  top: 50%;
  transform: translateY(-50%);
  width: 20px;
  height: 20px;
  border: 5px solid #191919;
  border-radius: 50%;
}

.card:nth-child(odd):after {
  content: '';
  position: absolute;
  right: -8.5%;
  top: 50%;
  transform: translateY(-50%);
  width: 7%;
  height: 2px;
  background: #fff;
  z-index: -1;
}

.card:nth-child(1) {
  margin-top: 0rem;
  background: #ff4f4f;
}

.card:nth-child(2) {
  background: #4f52ff;
}

.card:nth-child(3) {
  background: #3dcaae;
}

.card:before {
  background: var(--text-color);
}

.card-title {
  font-size: 2.5rem;
  text-align: center;
}

.card--detail {
  font-size: 12px;
}

.card--detail_short {
  font-size: 13px;
  text-align: center;

}
</style>