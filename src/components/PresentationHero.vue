<script setup>
import miCvPath from '../assets/CV_DiegoNuzzo.pdf';
</script>

<template>
    <section class="hero min-h-[70vh] bg-linear-to-b from-transparent to-black/70  px-10 ">

        <div class="hero-content flex-col lg:flex-row justify-between w-full">


            <div class="text-left flex-1 max-w-2x">
                <div class="group relative">
                    <h1
                        class="text-6xl font-black leading-none group-hover:text-accent transition-all duration-300 cursor-default">
                        Diego Nuzzo
                        <span class="text-lg font-light badge badge-accent ">Trainee</span>
                    </h1>

                    <div
                        class="max-h-0 opacity-0 group-hover:max-h-96 group-hover:opacity-100 overflow-hidden transition-all duration-500 ease-in-out">
                        <div class="mt-4 p-4 bg-base-200 border-l-4 border-accent rounded-r-lg shadow-md">
                            <h3 class="font-bold text-accent mb-2">Mi Perfil Profesional</h3>
                            <p class="leading-relaxed">
                                Estudiante de Informática con sólida formación en desarrollo de software y análisis de
                                sistemas. Cuento con experiencia práctica en la proyección y la creación de prototipos
                                funcionales especialmente utilizando lenguajes como Ruby, Java y C#. Poseo habilidades
                                en la organización de flujos de trabajo mediante herramientas de gestión como Trello. Me
                                destaco por mi capacidad de aprendizaje y trabajar en entornos bajo presión, siempre
                                busco soluciones técnicas que cumplan con los estándares de calidad de la organización.
                            </p>
                        </div>
                    </div>
                </div>
                <div class="mt-5 flex gap-4">
                    <a href="https://www.linkedin.com/in/nuzzodev" target="_blank" rel="noopener noreferrer"
                        class="btn btn-accent">
                        LinkedIn
                    </a>
                    <a :href="miCvPath" download="CV_Diego_Nuzzo.pdf"
                        class="btn btn-outline hover:bg-white hover:text-accent hover:border-white">
                        Ver CV
                    </a>
                </div>
            </div>

            <div class="flex-1 flex justify-center lg:justify-end relative ">


                <img src="../assets/Nuzzo.webp"
                    class="max-w-md w-full  relative z-10 drop-shadow-2xl border-4 rounded-xl"
                    alt="Foto de Diego Nuzzo" />
            </div>

        </div>
    </section>
</template>