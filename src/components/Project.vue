<script setup>
import { ref } from 'vue';
const projects = ref([

    {
        img: new URL('../assets/img/ecommerce.jpeg', import.meta.url).href,
        name: 'Tienda Virtual'
    },
    {
        img: new URL('../assets/img/app-pos.jpeg', import.meta.url).href,
        name: 'Sistema Pos para celulares'
    },
    {
        img: new URL('../assets/img/porfolio-grupa.jpeg', import.meta.url).href,
        name: 'Porfolio grupal'
    }

])
</script>
<template>
    <section id="projects" class="projects">
        <h1 class="section_title">Proyectos</h1>
        <article class="projects__container">
            <div  v-for= "project in projects" class="card_projects headline">
                <div class="card__image">
                    <img :src="project.img" alt="tienda virtual">
                </div>
                <h3>{{ project.name }}</h3>
            </div>
        </article>
    </section>
</template>
<style scoped>
.projects__container {
    gap: 30px;
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    margin-bottom: 10rem;
}

.card_projects {
    flex: 100%;
    box-shadow: var(--shadow);
    border-radius: 10px;
    padding: 10px 20px;
    background-color: transparent;
    overflow: hidden;
}

.card_projects .card__image {
    position: relative;
    width: 100%;
    height: 200px;
    border-radius: 1rem;
    display: flex;
    overflow: hidden;
}

.card_projects .card__image::before {
    position: absolute;
    content: '';
    width: 110%;
    height: 21p;
    border-bottom: 40px solid var(--color-secondary);
    opacity: .2;
    z-index: 1004;
    left: -10px;
    top: 170px;
    transform: rotate(5deg)
}

.card_projects .card__image img {
    width: 100%;
    height: 100%;
    opacity: .9;
}

.card_projects h3 {
    font-size: 1.5rem;
    margin-top: 15px;
    color: var(--title-color);
}

.card_projects p {
    font-size: 1.5rem;
    color: var(--text-color);
}

.card_projects_header a i {
    border-radius: 25px;
    color: var(--title-color);
    font-size: 30px;
    /* animation: gitAnimate duration timing-function delay iteration-count direction fill-mode; */
    animation: gitAnimate 4s ease-in infinite;
    animation-delay: 3s;
}

@keyframes gitAnimate {
    0% {
        color: var(--title-color);
    }

    50% {
        color: var(--title-color);
    }

    75% {
        color: var(--color-secondary);
    }

    100% {
        color: var(--title-color);
    }
}

/* responsive */
@media (min-width: 650px) {
    .card_projects {
        flex: 10%;
    }

    .row {
        display: flex;
        gap: 50px;
        justify-content: flex-start;
        align-items: center;
        flex-wrap: nowrap;
    }
}

@media (min-width: 460px) {
    .card_projects {
        flex: 30px;
    }
}
</style>