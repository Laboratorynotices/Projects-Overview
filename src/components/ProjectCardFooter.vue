<script setup>
    import TechnologyCard from '@/components/TechnologyCard.vue'
    defineProps({
        url: String,
        gitHubUrl: String,
        technologies: Array 
    })
</script>

<template>
    <footer class="flex justify-between border-t border-gray-300 px-8 py-4 mt-auto">
        <div>
            <a
                :href="url" target="_blank"
                class="rounded-full bg-blue-600 p-2 mr-3 shadow text-white hover:bg-blue-700 dark:bg-blue-300 dark:hover:bg-blue-200"
            >
                Demo
            </a>
            <a
                v-if="gitHubUrl"
                :href="gitHubUrl"
                target="_blank"
                class="rounded-full bg-blue-600 p-2 mr-3 shadow text-white hover:bg-blue-700 dark:bg-blue-300 dark:hover:bg-blue-200"
            >
                GitHub
            </a>
        </div>
        <div class="h-full flex flex-row-reverse">
            <!-- Вызов данных по отдельности. -->
            <TechnologyCard
                v-for="(technology, index) in technologies"
                :key="index"
                :technology="technology"
                mode="ProjectCardFooter"
            />
        </div>
    </footer>
</template>
