<script setup>
    defineProps({
        project: Object
    })
</script>

<template>
    <!-- Карточка для отображения проекта -->
    <article class="my-2 rounded-lg shadow-lg bg-white flex flex-col">
        <!-- Заголовок карточки -->
        <header>
            <h1
                class="text-3xl font-bold border-b border-gray-300">
                {{ project.name }}
            </h1>
        </header>

        <!-- Описание проекта -->
        <div class="h-fit">
            <p>{{ project.description }}</p>
        </div>

        <!-- Подвал карточки -->
        <footer class="border-t border-gray-300  mt-auto">
            <a :href="project.url" target="_blank">Open</a>
            {{ project.technologies }}
        </footer>
    </article>
</template>
