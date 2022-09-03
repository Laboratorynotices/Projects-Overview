<script setup>
    defineProps({
        text: String
    })
</script>

<template>
    <!-- Описание проекта -->
    <div class="px-8 py-4">
        <p>{{ text }}</p>
    </div>
</template>
