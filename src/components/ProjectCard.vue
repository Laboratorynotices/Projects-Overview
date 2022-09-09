<script setup>
    import ProjectCardHeader    from '@/components/ProjectCardHeader.vue'
    import ProjectCardMain      from '@/components/ProjectCardMain.vue'
    import ProjectCardFooter    from '@/components/ProjectCardFooter.vue'

    defineProps({
        project: Object
    })
</script>

<template>
    <!-- Карточка для отображения проекта -->
    <article class="my-2 rounded-3xl shadow-lg bg-white dark:bg-gradient-to-br dark:from-blue-700 dark:to-blue-500 flex flex-col">
        <!-- Заголовок карточки -->
        <ProjectCardHeader :title="project.name" />

        <!-- Описание проекта -->
        <ProjectCardMain :text="project.description" />

        <!-- Подвал карточки -->
        <ProjectCardFooter
            :url="project.url"
            :technologies="project.technologies"
            :gitHubUrl="project.gitHubUrl"
        />
    </article>
</template>
