<script setup lang="ts">
import { ref } from 'vue';

const mission = ref(`Proveer soluciones avanzadas de monitoreo y análisis de datos mediante telemetría inteligente, potenciando decisiones precisas en sectores productivos como la agricultura, psicultura, industria y medio ambiente.`);
const vision = ref(`Ser referentes en innovación tecnológica para monitoreo en tiempo real, liderando la transformación digital en Latinoamérica con soluciones eficientes, seguras y sostenibles.`);
const sections = [
  {
    title: 'Agricultura Inteligente',
    description: 'Optimización del riego, monitoreo del clima y suelo en tiempo real.',
    image: '/img/agricultura.jpg',
  },
  {
    title: 'Psicultura de Precisión',
    description: 'Control continuo de parámetros críticos como oxígeno y temperatura.',
    image: '/img/psicultura.jpg',
  },
  {
    title: 'Industria y Logística',
    description: 'Monitoreo de variables en procesos industriales y cadena de frío.',
    image: '/img/industria.jpg',
  },
];
</script>

<template>
  <div class="min-h-screen bg-gradient-to-b from-white via-gray-100 to-white dark:from-gray-900 dark:via-gray-800 dark:to-gray-900 text-gray-800 dark:text-white py-16 px-6">
    <div class="max-w-6xl mx-auto text-center space-y-12">

      <div>
        <h1 class="text-5xl font-extrabold text-green-600 dark:text-green-400 mb-4">Telesens Chile</h1>
        <p class="text-lg md:text-xl max-w-2xl mx-auto">
          Plataforma avanzada de <strong>telemetría</strong> para monitoreo en tiempo real de sensores en diversas industrias.
        </p>
      </div>

      <!-- Misión y visión -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8 text-left">
        <div class="bg-white dark:bg-gray-800 p-6 rounded-xl shadow">
          <h2 class="text-2xl font-semibold text-green-700 dark:text-green-300 mb-2">Nuestra Misión</h2>
          <p>{{ mission }}</p>
        </div>
        <div class="bg-white dark:bg-gray-800 p-6 rounded-xl shadow">
          <h2 class="text-2xl font-semibold text-green-700 dark:text-green-300 mb-2">Nuestra Visión</h2>
          <p>{{ vision }}</p>
        </div>
      </div>

      <!-- Sectores -->
      <div>
        <h2 class="text-3xl font-bold mb-6 text-green-600 dark:text-green-400">Áreas de Aplicación</h2>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
          <div
            v-for="(section, i) in sections"
            :key="i"
            class="bg-white dark:bg-gray-900 rounded-xl shadow-lg overflow-hidden"
          >
            <img :src="section.image" alt="" class="w-full h-40 object-cover" />
            <div class="p-4">
              <h3 class="text-xl font-bold text-green-700 dark:text-green-300">{{ section.title }}</h3>
              <p class="text-sm mt-2 text-gray-700 dark:text-gray-300">{{ section.description }}</p>
            </div>
          </div>
        </div>
      </div>

      <!-- Botón al sistema -->
      <div class="pt-10">
        <a
          href="https://app.telesens.cl"
          target="_blank"
          rel="noopener"
          class="inline-block bg-green-600 hover:bg-green-700 text-white px-8 py-4 rounded-full text-lg font-semibold transition"
        >
          Ingresar a la Plataforma
        </a>
      </div>

    </div>
  </div>
</template>
