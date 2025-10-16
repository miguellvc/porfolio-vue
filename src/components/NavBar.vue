<script setup>
import { ref } from 'vue';
const navegacion = ref([
    { id: 1, nombre: 'Inicio', enlace: 'inicio' },
    { id: 2, nombre: 'Educación', enlace: 'educacion' },
    { id: 3, nombre: 'Habilidad', enlace: 'habilidad' },
    { id: 4, nombre: 'Proyectos' }
])
</script>
<template>

    <ul class="menu">
        <div class="logo">
            <img src="./src/img/logo.png" alt="logo">
        </div>
        <ul class="navbar">
            <li v-for="nav in navegacion" :key="nav.nombre"><a href="nav.enlace">{{ nav.nombre }}</a></li>
        </ul>
    </ul>

</template>

<style scoped>
.menu {
    width: 90%;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.logo {
    display: flex;
    align-items: center;
}

.navbar {
    display: flex;
    gap: 1rem;
    list-style: none;
}

.navbar li a {
    text-decoration: none;
    color: var(--title-color);
    font-weight: 500;
    font-size: 2rem;
}

.logo img {
    width: 4rem;
    border-radius: 20px;
    color: var(--title-color);
}

.navbar {
    display: flex;
    gap: 1.5rem;
    list-style: none;
}

.navbar li a {
    text-decoration: none;
    color: var(--title-color);
    font-weight: 500;
    transition: color 0.3s ease;
}

.navbar li a:hover {
    color: var(--text-color);
    border-bottom: 2px solid;
}

/* Responsive: menú */

@media (max-width: 580px) {
    .menu {
        width: 100%;
        justify-content: flex-start;
        gap: 2rem;
    }
}
</style>