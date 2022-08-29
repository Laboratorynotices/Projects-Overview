<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <ProjectsSection :projects="projects" />
  <HelloWorld msg="Welcome to Your Vue.js App"/>
</template>

<script setup>
import HelloWorld from './components/HelloWorld.vue'
import ProjectsSection from './components/ProjectsSection.vue'

const projects =
  [
    {
      name: 'Vogelsberg',
      url: 'google.com',
      description : 'Uhu-hu-hu uhu uhu. Uhu-hu-hu uhu uhu. Uhu-hu-hu uhu uhu. Uhu-hu-hu uhu uhu. Uhu-hu-hu uhu uhu. Uhu-hu-hu uhu uhu. Uhu-hu-hu uhu uhu. ',
      technologies : ['vue', 'html'],
    },
    {
      name: 'Steinhaufen',
      url: 'google.de',
      description : 'Aha-hu-ha ahu uha. Uhu-hu-hu uhu uhu. Uhu-hu-hu uhu uhu. Uhu-hu-hu uhu uhu. Uhu-hu-hu uhu uhu. ',
      technologies : ['cakephp', 'html'],
    },
    {
      name: 'Wassertahl',
      url: 'google.at',
      description : 'Tropf-Tropf, Tropf, Tropf, Tropf-Tropf. Tropf.',
      technologies : ['yii2', 'html'],
    },
  ]

</script>

<style lang="less">
</style>
