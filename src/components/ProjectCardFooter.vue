<script setup>
    defineProps({
        url: String,
        technologies: Array 
    })
</script>

<template>
    <footer class="border-t border-gray-300 px-8 py-4 mt-auto">
        <a
            :href="url" target="_blank"
            class="rounded-full bg-blue-600 p-2 shadow text-white hover:bg-blue-700"
        >
            Open
        </a>
        <div class="float-right">
            {{ technologies }}
        </div>
    </footer>
</template>
