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
        <div class="container mx-auto grid grid-cols-6 gap-8 py-16 md:py-20 md:grid-cols-12">

            <!-- Вызов данных по отдельности. -->
            <TechnologyCard
                v-for="(technology, index) in technologies"
                :key="index"
                :technology="technology"
            />

        </div>
    </section>
</template>
