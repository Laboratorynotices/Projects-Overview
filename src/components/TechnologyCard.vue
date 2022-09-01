<script setup>
    defineProps({
        technology: String
    })
</script>

<template>
    <!-- Логотипы технологий должны быть .svg-формата и иметь такое же имя, которое у технологии -->
    <!-- Рамка и тень вокруг логотипов -->
    <div class="my-2 rounded-full border-4 ring-offset-current border-blue-700 shadow-xl">
        <!-- Отображение самих логотипов -->
        <div
            class="rounded-full aspect-square bg-no-repeat bg-center bg-contain bg-white"
            :style="'background-image: url(\'img/technologies/' + technology + '.svg\')'"
            :title="technology"
        />
    </div>
</template>
