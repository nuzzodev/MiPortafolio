<script setup>

import ProjectsCard from './CardsComponents/ProjectCard.vue'; 
import Ajeate from '../assets/Ajeate.PNG';
import Portafolio from '../assets/Portafolio.PNG';
</script>

<template>
  <section class="py-24 px-6 relative bg-black/70">
    <div class="max-w-6xl mx-auto relative z-10">
      
      <div class="text-center mb-20">
        <h2 class="text-6xl font-black mb-4 uppercase tracking-tighter">
          Mis <span class="text-accent">Proyectos</span>
        </h2>
        <div class="divider w-32 mx-auto divider-accent"></div>
      </div>

      <div class="flex flex-col gap-12">
        <ProjectsCard 
          title="Ajeate"
          description="Desarrollo de un DSS (Decision Support System) orientado a la administración de stocks y logística de pedidos. Implementado bajo una arquitectura Full-Stack utilizando Ruby on Rails, este proyecto combina una lógica de negocio robusta con una interfaz de usuario intuitiva y de alto rendimiento, diseñada para facilitar la toma de decisiones estratégicas."
          :image="Ajeate"
          :tags="['VueJs','Bootstrap','Rails', 'PostgreSQL']"
          borderColor="border-accent" 
          bgColor="bg-accent" 
          textColor="text-accent"
          irA="https://github.com/nuzzodev/Ajeate"
        />

        <ProjectsCard 
          title="Mi Portafolio"
          description="Este portafolio es un proyecto diseñado bajo una arquitectura de componentes reactivos con Vue 3 y estilizado con Tailwind CSS y DaisyUi, para demostrar mi capacidad de presentar mis capacidades técnicas en interfaces web."
          :image="Portafolio" 
          :tags="['Vue.js','Tailwind', 'DaisyUi']"
          borderColor="border-primary" 
          bgColor="bg-primary" 
          textColor="text-primary"
          irA="https://github.com/nuzzodev/MiPortafolio"
        />
      </div>

    </div>
  </section>
</template>