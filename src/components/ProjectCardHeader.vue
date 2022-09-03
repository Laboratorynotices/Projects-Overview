<script setup>
    defineProps({
        title: String
    })
</script>

<template>
    <header
        class="border-b border-gray-300 px-8 py-4"
    >
        <h1
            class="text-3xl font-bold"
        >
            {{ title }}
        </h1>
    </header>
</template>
