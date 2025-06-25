<script setup lang="ts">
import { ref } from 'vue';

const mission = ref(`Proveer soluciones avanzadas de monitoreo y análisis de datos mediante telemetría inteligente, potenciando decisiones precisas en sectores productivos como la agricultura, psicultura, industria y medio ambiente.`);
const vision = ref(`Ser referentes en innovación tecnológica para monitoreo en tiempo real, liderando la transformación digital en Latinoamérica con soluciones eficientes, seguras y sostenibles.`);

const sections = [
  {
    id: 'agricultura',
    title: 'Agricultura Inteligente',
    description: 'Optimización del riego, monitoreo del clima y suelo en tiempo real.',
    image: '/img/agricultura.jpg',
  },
  {
    id: 'psicultura',
    title: 'Psicultura de Precisión',
    description: 'Control continuo de parámetros críticos como oxígeno y temperatura.',
    image: '/img/psicultura.jpg',
  },
  {
    id: 'industria',
    title: 'Industria y Logística',
    description: 'Monitoreo de variables en procesos industriales y cadena de frío.',
    image: '/img/industria.jpg',
  },
];
</script>

<template>
  <div
    class="min-h-screen font-sans2 bg-gradient-to-b from-white via-gray-100 to-white dark:from-gray-900 dark:via-gray-800 dark:to-gray-900 text-gray-800 dark:text-white scroll-mt-24">
    <main class="max-w-6xl mx-auto pt-12 px-6 space-y-20">

      <!-- Inicio -->
      <section id="inicio" class="text-center space-y-4">
        <h1 class="text-6xl font-extrabold text-green-600 dark:text-green-400 leading-tight">
          Telesens Chile
        </h1>
        <p class="max-w-3xl mx-auto text-xl md:text-2xl leading-relaxed">
          Plataforma avanzada de <strong>telemetría</strong> para monitoreo en tiempo real de sensores en diversas
          industrias.
        </p>
        <a href="https://app.telesens.cl"
          class="inline-block mt-8 bg-green-600 hover:bg-green-700 text-white px-10 py-4 rounded-full text-xl font-semibold transition">
          Ingresar a la Plataforma
        </a>
      </section>

      <!-- Sobre Nosotros -->
      <section id="sobre-nosotros"
        class="grid grid-cols-1 md:grid-cols-2 gap-12 bg-white dark:bg-gray-800 p-8 rounded-xl shadow-lg">
        <div>
          <h2 class="text-3xl font-bold mb-6 text-green-700 dark:text-green-300">Nuestra Misión</h2>
          <p class="text-lg leading-relaxed">{{ mission }}</p>
        </div>
        <div>
          <h2 class="text-3xl font-bold mb-6 text-green-700 dark:text-green-300">Nuestra Visión</h2>
          <p class="text-lg leading-relaxed">{{ vision }}</p>
        </div>
      </section>

      <!-- Áreas -->
      <section id="servicios">
        <h2 class="text-4xl font-bold mb-10 text-center text-green-600 dark:text-green-400">Áreas de Aplicación</h2>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <article v-for="section in sections" :key="section.id"
            class="bg-white dark:bg-gray-900 rounded-xl shadow-lg overflow-hidden flex flex-col">
            <img :src="section.image" :alt="section.title" class="w-full h-48 object-cover" loading="lazy" />
            <div class="p-6 flex flex-col flex-grow">
              <h3 class="text-2xl font-semibold mb-2 text-green-700 dark:text-green-300">{{ section.title }}</h3>
              <p class="text-gray-700 dark:text-gray-300 flex-grow leading-relaxed text-sm md:text-base">
                {{ section.description }}
              </p>
            </div>
          </article>
        </div>
      </section>

      <!-- Contacto -->
      <section id="contacto" class="bg-white dark:bg-gray-800 p-8 rounded-xl shadow-lg max-w-3xl mx-auto">
        <h2 class="text-3xl font-bold mb-6 text-green-700 dark:text-green-300 text-center">
          Contáctanos
        </h2>

        <form action="mailto:Freddy_andres@hotmail.es" method="POST" class="flex flex-col space-y-4"
          enctype="text/plain">
          <input type="text" name="Nombre" placeholder="Nombre de contacto" required
            class="p-3 rounded border border-gray-300 dark:border-gray-600 bg-white dark:bg-gray-700 text-gray-900 dark:text-white focus:outline-none focus:ring-2 focus:ring-green-500" />
          <input type="text" name="Asunto" placeholder="Asunto" required
            class="p-3 rounded border border-gray-300 dark:border-gray-600 bg-white dark:bg-gray-700 text-gray-900 dark:text-white focus:outline-none focus:ring-2 focus:ring-green-500" />
          <textarea name="Mensaje" placeholder="Mensaje" rows="5" required
            class="p-3 rounded border border-gray-300 dark:border-gray-600 bg-white dark:bg-gray-700 text-gray-900 dark:text-white focus:outline-none focus:ring-2 focus:ring-green-500 resize-none"></textarea>
          <button type="submit"
            class="bg-green-600 hover:bg-green-700 text-white py-3 rounded font-semibold transition">
            Enviar mensaje
          </button>
        </form>
      </section>
      
    </main>
  </div>
</template>