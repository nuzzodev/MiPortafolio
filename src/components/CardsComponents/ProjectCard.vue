<template>
  <div :class="['card bg-base-100/50 backdrop-blur-md shadow-2xl border-l-8 overflow-hidden group transition-all hover:bg-base-100/80', borderColor]">
    <div class="flex flex-col lg:flex-row min-h-87.5">
      
      <div class="w-full lg:w-1/3 relative overflow-hidden bg-base-300">
        <div :class="['absolute inset-0 opacity-0 group-hover:opacity-20 transition-opacity z-10', bgColor]"></div>
        
        <img 
          :src="image" 
          :alt="title" 
          class="w-full h-full object-cover object-top transition-transform duration-500 group-hover:scale-105"
        />
      </div>

      <div class="w-full lg:w-2/3 p-8 md:p-12 flex flex-col justify-center">
        <div class="mb-4">
          <span :class="['text-xs font-bold uppercase tracking-[0.2em] mb-2 inline-block', textColor]">
            Proyecto Seleccionado
          </span>
          <h3 class="text-4xl font-black uppercase tracking-tighter leading-none">
            {{ title }}
          </h3>
        </div>

        <p class="text-lg opacity-80 leading-relaxed mb-6 max-w-2xl">
          {{ description }}
        </p>

        <div class="flex flex-wrap gap-3 mb-6">
          <span v-for="tag in tags" :key="tag" 
                class="px-3 py-1 bg-base-content/5 rounded-md text-[10px] font-bold uppercase tracking-widest opacity-60 border border-base-content/10">
            {{ tag }}
          </span>
        </div>
        <a :href="irA" 
             target="_blank" 
             rel="noopener noreferrer" 
             class="btn btn-outline gap-2 group/btn transition-all hover:bg-white hover:text-black"
             :class="textColor"> 
            <i class="devicon-github-original text-xl transition-transform group-hover/btn:scale-110"></i>
            Ir al código Fuente
        </a>  
      </div>

    </div>
  </div>
</template>

<script setup>
defineProps({
  title: String,
  description: String,
  image: String,
  tags: Array,
  borderColor: String,
  bgColor: String,
  textColor: String,
  irA:String
});
</script>