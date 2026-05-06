<script setup>
    import ProjectCard from './ProjectCard.vue';
</script>

<template>
    <section id="projects" class="projects">
        <div class="container">
            <h2 class="projects__title">My <span class="bold">Projects</span></h2>
            <div class="projects__cards">
                <ProjectCard
                    image = "/src/assets/img/Desserts_img.jpg"
                    title = "Desserts"
                    description = "An interactive dessert menu with cart functionality. Users can add and remove items, calculate total cost, and place an order. Built using vanilla HTML, CSS, and JavaScript."
                    link = "https://skippy-hub.github.io/Frontend-Mentor/"
                />
                <ProjectCard
                    image = "/src/assets/img/Art_img.jpg"
                    title = "Art"
                    description = "A one-page landing page with a product catalog and filtering by author country. Implemented interactive filtering and responsive layout. Built with Vue.js, HTML, SCSS, and JavaScript."
                    link = "https://art-sable-alpha.vercel.app/"
                />
                <ProjectCard
                    image = "/src/assets/img/Blanko_img.jpg"
                    title = "Blanko"
                    description = "One-page responsive landing page with company information and contact section. Adapted for desktop and mobile devices. Built using Vue.js, HTML, SCSS, and JavaScript."
                    link = "https://blanko-gamma.vercel.app/"
                />              
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    .projects{
        background: #000;
        padding: 8rem 5rem 6rem;

        @media (max-width: 979px) {
            padding: 5rem;
            margin-top: -4rem;
        }
        
        @media (max-width: 480px) {
            padding: 5rem 2rem 5rem;
        }

        &__title{
            color: #fff;
            text-align: center;
            margin-bottom: 2rem;
            font-size: 3rem;
            line-height: 116%;

            @media (max-width: 979px) {
                font-size: 2rem;
                line-height: 100%;
            }

            @media (max-width: 480px) {
                font-size: 1.5rem;   
            }
        }

        &__cards{
            display: grid;
            grid-template-columns: repeat(3, auto);
            gap: 2rem;

            @media (max-width: 979px) {
                grid-template-columns: auto;
                justify-content: center;
            }
        }
    }
</style>