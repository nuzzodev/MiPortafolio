<script setup>
defineProps({
  title: String,
  subtitle: String,
  badgeColor: { type: String, default: 'badge-secondary' }
});
</script>

<template>
  <div class="flex items-center gap-4 group cursor-default">
    <div :class="['badge badge-xs shrink-0', badgeColor]"></div>
    <div class="flex flex-col">
      <span class="text-sm font-black uppercase tracking-widest text-white group-hover:text-secondary transition-colors">
        {{ title }}
      </span>
      <span class="text-[10px] font-bold text-base-content/50 uppercase italic">
        {{ subtitle }}
      </span>
    </div>
  </div>
</template>