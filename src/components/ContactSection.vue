<script setup>
const FORM_ID = "ypnusi2zrwm"; 

const handleSubmit = async (event) => {
  const formData = new FormData(event.target);
  
  try {
    const response = await fetch(`https://forminit.com/f/${FORM_ID}`, {
      method: "POST",
      body: formData,
      headers: {
        'Accept': 'application/json'
      }
    });

    if (response.ok) {
      alert("¡Mensaje enviado con éxito!");
      event.target.reset(); 
    } else {
      throw new Error("Error en la respuesta del servidor");
    }
  } catch (err) {
    console.error("Error al enviar:", err);
    alert("Hubo un problema al enviar el formulario. Inténtalo de nuevo.");
  }
};
</script>

<template>
  <section class="py-20 px-6 relative bg-black/70">
    <div class="max-w-4xl mx-auto relative z-10">
      
      <div class="text-center mb-16">
        <h2 class="text-5xl font-black mb-4 uppercase tracking-tighter">
          Contacto <span class="text-accent">Directo</span>
        </h2>
        <div class="divider w-24 mx-auto divider-accent"></div>
      </div>

      <form 
        @submit.prevent="handleSubmit" 
        class="grid grid-cols-1 md:grid-cols-2 gap-8 bg-base-200 p-6 rounded-2xl"
      >
        <div class="flex flex-col">
          <label class="uppercase font-black text-sm mb-2 text-accent tracking-tighter">Nombre</label>
          <input 
            type="text" 
            name="fi-sender-firstName" 
            required
            class="bg-black border-2 border-accent p-4 text-white focus:outline-none rounded-2xl"
            placeholder="Tu nombre completo"
          >
        </div>

        <div class="flex flex-col">
          <label class="uppercase font-black text-sm mb-2 text-accent tracking-tighter">Correo</label>
          <input 
            type="email" 
            name="fi-sender-email" 
            required
            class="bg-black border-2 border-accent p-4 text-white focus:outline-none rounded-2xl"
            placeholder="tu@email.com"
          >
        </div>

        <div class="flex flex-col md:col-span-2">
          <label class="uppercase font-black text-sm mb-2 text-accent tracking-tighter">Asunto</label>
          <input 
            type="text" 
            name="fi-text-subject" 
            required
            class="bg-black border-2 border-accent p-4 text-white focus:outline-none rounded-2xl"
            placeholder="¿Sobre qué quieres hablar?"
          >
        </div>

        <div class="flex flex-col md:col-span-2">
          <label class="uppercase font-black text-sm mb-2 text-accent tracking-tighter">Contenido</label>
          <textarea 
            name="fi-text-message" 
            rows="5" 
            required
            class="bg-black border-2 border-accent p-4 text-white focus:outline-none resize-none rounded-2xl"
            placeholder="Escribe tu mensaje aquí..."
          ></textarea>
        </div>

        <div class="md:col-span-2 text-center mt-4">
          <button 
            type="submit" 
            class="btn btn-accent text-base-300 font-black uppercase"
          >
            Enviar Mensaje
          </button>
        </div>
      </form>

    </div>
  </section>
</template>