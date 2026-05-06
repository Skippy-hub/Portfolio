<script setup>

</script>

<template>
    <section id="about" class="about">
        <div class="container container--flex">
            <img class="about__img" src="../assets/img/About_img.png" alt="">
            <div class="about__block">
                <h2 class="about__block-title">About <span class="bold">Me</span></h2>
                <div class="about__block-text">
                    <p class="about__block-text-par">I am a Junior Frontend Developer focused on building responsive and user-friendly web interfaces. I work with HTML, CSS, JavaScript, and modern tools to create clean and accessible UI. I am eager to grow professionally and contribute to real-world projects.</p>
                    <p class="about__block-text-par">When I'm not in full-on developer mode, you can find me hovering around on telegram, witnessing the journey of early startups or enjoying some free time. You can follow me on GitHub where I build in public.</p>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    .container--flex{
        display: flex;
        justify-content: space-between;
        gap: 2rem;

        @media (max-width: 767px) {
            flex-direction: column;            
        }
    }
    
    .about{
        margin-top: -6rem;
        padding: 6rem 5rem 3.75rem;

        @media (max-width: 979px) {
            margin-top: -3rem;
            padding: 6rem 5rem;
        }

        @media (max-width: 767px) {
            padding: 6rem 2rem;            
        }

        &__img{
            max-width: 25rem;
            width: 100%;
            height: 100%;

            @media (max-width: 767px) {
                max-width: 15rem;
                margin: 0 auto;   
            }

            @media (max-width: 480px) {
                display: none;
            }
        }

        &__block{
            max-width: 42rem;
            width: 100%;

            &-title{
                font-size: 3rem;
                line-height: 116%;
                margin-bottom: 2.5rem;

                @media (max-width: 1200px) {
                    margin-bottom: 1.5rem;
                }

                @media (max-width: 979px) {
                    font-size: 2rem;
                    line-height: 100%;
                }

                @media (max-width: 480px) {
                    font-size: 1.5rem;
                    text-align: center;   
                }
            }

            &-text{
                display: flex;
                flex-direction: column;
                gap: 1.25rem;

                &-par{
                    font-size: 1rem;
                    line-height: 150%;
                    color: #71717a;

                    @media (max-width: 979px) {
                        font-size: 0.75rem;
                        line-height: 125%;
                    }
                }
            }
        }
    }
</style>