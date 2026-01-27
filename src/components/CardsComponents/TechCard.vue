<template>
  <div :class="['card bg-base-100 shadow-xl  border-t-6 transition-all duration-300', borderColor]">
    <div class="card-body">
      
      <div class="flex items-center gap-3 mb-6">
        <div :class="['p-2 rounded-lg flex items-center justify-center w-10 h-10', bgColor, textColor]">
          <slot name="header-icon"></slot>
        </div>
        <h3 class="card-title text-xl font-black uppercase tracking-tighter">{{ title }}</h3>
      </div>

      <div class="grid grid-cols-3 gap-x-2 gap-y-6">
        <div v-for="tech in items" :key="tech.name" class="flex flex-col items-center group">
          
          <div :class="[
            'relative flex items-center justify-center transition-all duration-300',
            tech.featured ? 'scale-110' : ''
          ]">
            
            <div v-if="tech.featured" 
                 :class="['absolute mask mask-squircle w-[70px] h-[70px]', bgColor]">
            </div>

            <div :class="[
              'mask mask-squircle w-16 h-16 flex items-center justify-center z-10',
              tech.featured ? 'bg-base-100' : 'bg-base-200 group-hover:bg-base-300'
            ]">
              <i :class="[tech.icon, 'text-4xl']"></i>
            </div>
          </div>
          
          <span :class="[
            'mt-2 text-[10px] font-bold uppercase transition-opacity text-center',
            tech.featured ? 'opacity-100' : 'opacity-60'
          ]">
            {{ tech.name }}
          </span>
        </div>
      </div>

    </div>
  </div>
</template>
<script setup>
defineProps({
  title: String,
  borderColor: String,
  textColor: String,
  bgColor: String,
  items: Array,
  featured: Boolean 
});
</script>