<script setup lang="ts">
    interface Props {
        image: string;
        title: string;
        description: string;
        link: string;
    }

    const props = defineProps<Props>();
</script>

<template>
    <a :href="props.link" class="card" target="_blank">
        <img class="card__image" :src="props.image" alt="">
        <div class="card__block">
            <h3 class="card__block-title">{{ props.title }}</h3>
            <p class="card__block-description">{{ props.description }}</p>
        </div>
    </a>
</template>

<style lang="scss" scoped>
    .card{
        max-width: 25rem;
        width: 100%;
        padding: 1rem;
        display: flex;
        text-align: center;
        flex-direction: column;
        gap: 1rem;
        align-items: center;
        text-decoration: none;
        color: #fff;
        border: 2px solid #fff;
        border-radius: 0.25rem;
        transition: transform 0.3s ease;

        @media (max-width: 979px) {
            max-width: 20rem;
        }

        &:hover{
            transform: scale(1.05);
        }
        
        &__image{
            max-width: 17rem;
            height: 10rem;
            width: 100%;
        }

        &__block{
            display: flex;
            flex-direction: column;
            gap: 1rem;

            &-title{
                font-size: 1.75rem;
                font-weight: 600;
                
                @media (max-width: 1200px) {
                    font-size: 1.5rem;
                }
            }

            &-description{
                text-align: left;
                font-size: 1rem;
                line-height: 150%;
                color: #71717a;

                @media (max-width: 1200px) {
                    font-size: 0.75rem;
                }
            }
        }
    }
</style>