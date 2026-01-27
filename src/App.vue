<script setup>
import NavBar from './components/NavBar.vue';
import PresentationHero from './components/PresentationHero.vue';
import Stack from './components/Stack.vue';
import Projects from './components/Projects.vue';
import SkillsSection from './components/SkillsSection.vue';
</script>

<template>
  <NavBar/>
  <PresentationHero id="Inicio"/>
  <Stack id="stack"/>
  <SkillsSection id="habilidades"/>
  <Projects id="proyectos"/>
  
</template>