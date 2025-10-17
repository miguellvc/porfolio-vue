<script setup>
    import { ref } from 'vue'; 

    const banner = ref([
        {
            urlImg: new URL('../assets/img/Foto.jpeg', import.meta.url).href,
            content: {
                title: 'Hola, soy Miguel Perez.',
                subTitle : 'Sobre mí...',
                description : `Soy Técnico Universitario en Informática y actualmente estoy cursando la
                carrera de Técnico Universitario en Programación. Me gusta la tecnología, especialmente todo lo
                relacionado con el desarrollo de software. Disfruto aprender nuevas herramientas, enfrentar nuevos
                desafíos. Mi objetivo es seguir creciendo en el ámbito de la Informática y lograr formar parte de
                proyectos que involucren el desarrollo de software.`
            }
        }
    ])

    
</script>
<template>
    <section v-for="ban in banner" id="banner" class="banner">
        <article class="banner__img">
            <img :src="ban.urlImg" alt="foto_personal">
        </article>

        <article class="banner__content">
            <h2 class="content__title">{{ ban.content.title }}</h2>
            <h3 class="content__sub-title">{{ ban.content.subTitle }}</h3>
            <p class="content__description">{{ ban.content.description }}</p>
        </article>

    </section>
</template>

<style scoped>
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