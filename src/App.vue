<script setup>
import NavBar from './components/NavBar.vue';
import PresentationHero from './components/PresentationHero.vue';
import Stack from './components/Stack.vue';
import Projects from './components/Projects.vue';
import SkillsSection from './components/SkillsSection.vue';
import ContactSection from './components/ContactSection.vue';
import Footer from './components/Footer.vue';

import { onMounted } from 'vue'

onMounted(() => {
  const savedTheme = localStorage.getItem('theme');
  const htmlElement = document.documentElement;

  if (savedTheme) {
    // Si el usuario ya eligió uno manualmente, usamos ese
    htmlElement.setAttribute('data-theme', savedTheme);
  } else {
    const prefersDark = window.matchMedia('(prefers-color-scheme: dark)').matches;
    const initialTheme = prefersDark ? 'dark' : 'corporate';
    
    htmlElement.setAttribute('data-theme', initialTheme);
  }
});

</script>

<template>
  <NavBar/>

  <PresentationHero id="Inicio"/>
  <Stack id="stack"/>
  <SkillsSection id="habilidades"/>
  <Projects id="proyectos"/>
  <ContactSection id="contacto"/>
  <Footer/>
</template>