<script setup>
import SkillBadge from './CardsComponents/SkillBadge.vue';

const redSkills = [
  { name: 'Redes & Conectividad', desc: 'Conocimientos cursados en el 4to semestre de informática.' }, // [cite: 13]
  { name: 'Soporte Técnico', desc: 'Manejo de herramientas tecnológicas y mantenimiento.' }, // [cite: 16, 23]
  { name: 'Gestión de Proyectos', desc: 'Metodologías Ágiles, SCRUM y KANBAN.' }, // [cite: 18]
  { name: 'Herramientas IA', desc: 'Capacitación en el uso de IA y herramientas como Canva.' } // [cite: 23]
];

const softSkills = [
  { name: 'Responsabilidad', sub: 'Compromiso organizacional' }, // [cite: 18]
  { name: 'Proactivo', sub: 'Iniciativa en soluciones' }, // [cite: 18]
  { name: 'Adaptabilidad', sub: 'Entornos bajo presión' }, // [cite: 8, 18]
  { name: 'Trabajo en equipo', sub: 'Colaboración efectiva' }, // [cite: 18]
  { name: 'Paciencia', sub: 'Resolución de conflictos' } // [cite: 18]
];
</script>

<template>
  <section class="py-20 px-6 bg-black/70">
    <div class="max-w-6xl mx-auto">
      
      <div class="text-center mb-20">
        <h2 class="text-6xl font-black mb-4 uppercase tracking-tighter">
          Mis <span class="text-accent">Habilidades</span>
        </h2>
        <div class="divider w-32 mx-auto divider-accent"></div>
      </div>

      <div class="grid grid-cols-1 lg:grid-cols-12 gap-12">
        
        <div class="lg:col-span-8 space-y-8  border-l-5 rounded-xl ps-4 border-secondary">
          <div v-for="(skill, index) in redSkills" :key="index">
            <div class="flex gap-6 items-start">
              <span class="text-5xl font-black  text-accent italic">0{{ index + 1 }}</span>
              <div class="space-y-1">
                <h3 class="text-2xl font-black uppercase text-white tracking-tight">{{ skill.name }}</h3>
                <p class="text-sm text-base-content/70 leading-relaxed">{{ skill.desc }}</p>
              </div>
            </div>
            <div class="divider opacity-5 mt-4"></div>
          </div>
          
          
        </div>

        <div class="lg:col-span-4 flex flex-col gap-8 border-4 rounded-2xl border-accent bg-base-300 p-5">
          
          <div class="space-y-6">
            <h3 class="text-md font-bold  uppercase  flex items-center gap-2">
              Habilidades Blandas 
            </h3>
            
            <div class="flex flex-col gap-5 px-2">
              <SkillBadge 
                v-for="soft in softSkills" 
                :key="soft.name"
                :title="soft.name"
                :subtitle="soft.sub"
              />
            </div>
          </div>

          <div class="space-y-4">
            <h3 class="text-md font-bold  uppercase  flex items-center gap-2">
              Herramientas Complementarias
            </h3>
            <div class="flex flex-wrap gap-2">
              <div class="badge badge-outline badge-md font-bold px-4 py-3 opacity-60 hover:opacity-100 transition-opacity">TRELLO</div> <div class="badge badge-outline badge-md font-bold px-4 py-3 opacity-60 hover:opacity-100 transition-opacity">OFFICE</div> <div class="badge badge-outline badge-md font-bold px-4 py-3 opacity-60 hover:opacity-100 transition-opacity">SCRUM</div> </div>
          </div>

        </div>

      </div>
    </div>
  </section>
</template>