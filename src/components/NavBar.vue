<script setup lang="ts">
import ThemeSwitcher from './ThemeSwitcher.vue';

</script>

<template>
  <header class="sticky top-0 z-50 w-full">
    <div class="navbar bg-base-100 shadow-md px-4 md:px-8">
      
      <div class="flex-1">
        <a href="#Inicio">
          <h2 class="text-2xl font-black tracking-tighter hover:text-accent transition-colors cursor-pointer">
            Nuzzo<span class="text-accent">Dev</span>
          </h2>
        </a>
      </div>
      <ThemeSwitcher/>

      <div class="flex-none hidden md:block">
        <ul class="menu menu-horizontal p-0 gap-2">
          <li><a href="#stack" class="hover:text-accent transition-colors text-xl">Stack</a></li>
          <li><a href="#habilidades" class="hover:text-accent transition-colors text-xl">Habilidades</a></li>
          <li><a href="#proyectos" class="hover:text-accent transition-colors text-xl">Proyectos</a></li>
          <li>
            <a href="#contacto" class="btn btn-accent rounded-lg ml-2 text-xl">Contacto</a>
          </li>
        </ul>
      </div>

      <div class="flex-none md:hidden">
        <div class="dropdown dropdown-end">
          <label tabindex="0" class="btn btn-square btn-ghost">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" class="inline-block w-5 h-5 stroke-current">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
            </svg>
          </label>
          <ul tabindex="0" class="menu menu-sm dropdown-content mt-3 z-[1] p-2 shadow bg-base-100 rounded-box w-52">
            <li><a href="#stack">Stack</a></li>
            <li><a href="#habilidades">Habilidades</a></li>
            <li><a href="#proyectos">Proyectos</a></li>
            <li><a href="#contacto" class="text-accent font-bold">Contacto</a></li>
          </ul>
        </div>
      </div>

    </div>
  </header>
</template>