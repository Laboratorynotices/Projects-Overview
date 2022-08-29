<template>

  {{ technologies }}
  
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

const technologies = projects.map(function (project) {
    // Вытягиваем массивы с технологиями из списка проектов.
    return (project.technologies)
    // На выходе получаются двухмерные массивы технологий.
  }).reduce(function(pre, cur) {
    // Переделываем двухмерный массив в одномерный, но более длинный
    return pre.concat(cur)
    // На выходе получается одномерный массив с технологиями, но значения могут быть двойными
  }).reduce(function(pre, cur) {
    // Избавляемся от двойных значений в массиве

    // При первом проходе в аккамуляторе "pre" находится простая строчка String,
    // для нормальной работы превращаем его в массив.
    if (typeof pre === 'string' || pre instanceof String)
      pre = [pre]

    // Проверка есть ли это значение уже в результате
    if (pre.includes(cur)) {
      // Да, нынешний элемент уже находится в списке.
      // Ничего не делаем, просто возвращаем аккамулятор.
      return pre
    } else {
      // Этого значения ещё нет в списке,
      // Добавляем его в список.
      return pre.concat(cur)
    }

    // На выходе получается список технологий без повторений.
  })


</script>

<style lang="less">
</style>
