<script setup>
    import TechnologyCard from '@/components/TechnologyCard.vue'
    defineProps({
        technologies: Array
    })
</script>

<template>
    <!-- Задний фон блока -->
    <section id="technologiesSection" class="bg-blue-600">
        <!-- Основное поле блока будет посередине с неким отступом -->
        <div class="container mx-auto grid grid-cols-4 gap-8 py-16 md:py-20 sm:grid-cols-6 md:grid-cols-8 lg:grid-cols-10 xl:grid-cols-12">

            <!-- Вызов данных по отдельности. -->
            <TechnologyCard
                v-for="(technology, index) in technologies"
                :key="index"
                :technology="technology"
            />

        </div>
    </section>
</template>
