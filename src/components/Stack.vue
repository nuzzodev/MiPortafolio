<script setup>
import TechCard from './TechCard.vue';

const frontend = [
  { name: 'Vue.js', icon: 'devicon-vuejs-plain colored', featured:true },
  { name: 'JS', icon: 'devicon-javascript-plain colored' },
  { name: 'HTML5', icon: 'devicon-html5-plain colored' },
  { name: 'CSS3', icon: 'devicon-css3-plain colored' },
  { name: 'Tailwind', icon: 'devicon-tailwindcss-plain colored' },
  { name: 'Bootstrap', icon: 'devicon-bootstrap-plain colored' }
];

const backend = [
  { name: 'Rails', icon: 'devicon-rails-plain colored', featured:true},
  { name: 'Spring', icon: 'devicon-spring-plain colored' },
  { name: 'PostgreSQL', icon: 'devicon-postgresql-plain colored' }
];

const tools = [
  { name: 'GitHub', icon: 'devicon-github-original', featured:true},
  { name: 'Git', icon: 'devicon-git-plain colored' },
  { name: 'Trello', icon: 'devicon-trello-plain colored' }
];
</script>

<template>
  <section class="py-20 px-6 relative bg-black/70">
    <div class="max-w-6xl mx-auto relative z-10">
      
      <div class="text-center mb-16">
        <h2 class="text-5xl font-black mb-4 uppercase tracking-tighter">Mi <span class="text-accent">Stack</span></h2>
        <div class="divider w-24 mx-auto divider-accent"></div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-8 items-stretch">
        <TechCard title="Frontend" borderColor="border-primary" textColor="text-primary" bgColor="bg-primary" :items="frontend" >
          <template #header-icon>
            <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="black">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.75 17L9 20l-1 1h8l-1-1-.75-3M3 13h18M5 17h14a2 2 0 002-2V5a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
            </svg>
          </template>
        </TechCard>

        <TechCard title="Backend" borderColor="border-accent" textColor="text-accent" bgColor="bg-accent" :items="backend" >
          <template #header-icon>
            <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="black">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 12h14M5 12a2 2 0 01-2-2V6a2 2 0 012-2h14a2 2 0 012 2v4a2 2 0 01-2 2M5 12a2 2 0 00-2 2v4a2 2 0 002 2h14a2 2 0 002-2v-4a2 2 0 00-2-2m-2-4h.01M17 16h.01" />
            </svg>
          </template>
        </TechCard>

        <TechCard title="Herramientas" borderColor="border-secondary" textColor="text-secondary" bgColor="bg-secondary" :items="tools">
          <template #header-icon>
            <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="black">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M11 4a2 2 0 114 0v1a1 1 0 001 1h3a1 1 0 011 1v3a1 1 0 01-1 1h-1a2 2 0 100 4h1a1 1 0 011 1v3a1 1 0 01-1 1h-3a1 1 0 01-1-1v-1a2 2 0 10-4 0v1a1 1 0 01-1 1H7a1 1 0 01-1-1v-3a1 1 0 00-1-1H4a2 2 0 110-4h1a1 1 0 001-1V7a1 1 0 011-1h3a1 1 0 001-1V4z" />
            </svg>
          </template>
        </TechCard>
      </div>

    </div>
  </section>
</template>