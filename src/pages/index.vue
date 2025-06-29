<script setup lang="ts">
import { ref, onMounted } from 'vue';

const mission = ref(`Proveer soluciones avanzadas de monitoreo y análisis de datos mediante telemetría inteligente, potenciando decisiones precisas en sectores productivos como la agricultura, psicultura, industria y medio ambiente.`);
const vision = ref(`Ser referentes en innovación tecnológica para monitoreo en tiempo real, liderando la transformación digital en Latinoamérica con soluciones eficientes, seguras y sostenibles.`);

const isVisible = ref(false);

onMounted(() => {
  setTimeout(() => {
    isVisible.value = true;
  }, 100);
});

const sections = [
  {
    id: 'agricultura',
    title: 'Agricultura Inteligente',
    description: 'Optimización del riego, monitoreo del clima y suelo en tiempo real para maximizar la productividad.',
    image: '/img/agricultura.jpg',
    icon: '🌱',
    features: ['Sensores de humedad', 'Monitoreo climático', 'Riego automatizado']
  },
  {
    id: 'psicultura',
    title: 'Psicultura de Precisión',
    description: 'Control continuo de parámetros críticos como oxígeno, temperatura y pH del agua.',
    image: '/img/psicultura.jpg',
    icon: '🐟',
    features: ['Control de oxígeno', 'Temperatura del agua', 'Calidad del agua']
  },
  {
    id: 'industria',
    title: 'Industria y Logística',
    description: 'Monitoreo de variables críticas en procesos industriales y cadena de frío.',
    image: '/img/industria.jpg',
    icon: '🏭',
    features: ['Cadena de frío', 'Procesos industriales', 'Logística inteligente']
  },
];

const stats = [
  { number: '1000+', label: 'Sensores Activos', icon: '📊' },
  { number: '50+', label: 'Clientes Satisfechos', icon: '🤝' },
  { number: '24/7', label: 'Monitoreo Continuo', icon: '⏰' },
  { number: '99.9%', label: 'Uptime Garantizado', icon: '🚀' }
];
</script>

<template>
  <div class="min-h-screen font-sans2 bg-white dark:bg-gray-900 text-gray-800 dark:text-white overflow-hidden">
    
    <!-- Hero Section con Gradiente Animado -->
    <section id="inicio" class="relative min-h-screen flex items-center justify-center overflow-hidden">
      <!-- Fondo animado con gradientes -->
      <div class="absolute inset-0 bg-gradient-to-br from-green-400 via-blue-500 to-purple-600 dark:from-green-600 dark:via-blue-700 dark:to-purple-800">
        <div class="absolute inset-0 bg-gradient-to-t from-black/20 to-transparent"></div>
        <!-- Formas geométricas animadas -->
        <div class="absolute top-10 left-10 w-32 h-32 bg-white/10 rounded-full blur-xl animate-pulse"></div>
        <div class="absolute bottom-20 right-20 w-48 h-48 bg-green-300/20 rounded-full blur-2xl animate-bounce" style="animation-duration: 3s;"></div>
        <div class="absolute top-1/2 left-1/4 w-24 h-24 bg-blue-300/20 rounded-full blur-lg animate-ping" style="animation-duration: 2s;"></div>
      </div>
      
      <!-- Contenido del Hero -->
      <div class="relative z-10 text-center space-y-8 px-6 max-w-5xl mx-auto" 
           :class="isVisible ? 'animate-fade-in-up' : 'opacity-0'">
        <div class="space-y-4">
          <h1 class="text-6xl md:text-8xl font-black text-white leading-tight">
            <span class="bg-gradient-to-r from-green-300 to-blue-300 bg-clip-text text-transparent">
              Telesens
            </span>
            <br>
            <span class="text-white text-shadow">Chile</span>
          </h1>
          <p class="text-xl md:text-3xl text-white/90 font-light max-w-4xl mx-auto leading-relaxed">
            Revolucionamos el <strong class="text-green-300">monitoreo inteligente</strong> 
            con telemetría avanzada para el futuro de la industria
          </p>
        </div>
        
        <div class="flex flex-col sm:flex-row gap-4 justify-center items-center pt-8">
          <a href="https://app.telesens.cl"
             class="group bg-white text-gray-900 px-8 py-4 rounded-full text-lg font-bold hover:bg-green-100 transition-all duration-300 transform hover:scale-105 shadow-2xl">
            <span class="flex items-center gap-2">
              Ingresar a la Plataforma
              <span class="group-hover:translate-x-1 transition-transform">→</span>
            </span>
          </a>
          <a href="#servicios"
             class="border-2 border-white text-white px-8 py-4 rounded-full text-lg font-bold hover:bg-white hover:text-gray-900 transition-all duration-300 transform hover:scale-105">
            Conocer Más
          </a>
        </div>
      </div>

      <!-- Scroll indicator -->
      <div class="absolute bottom-8 left-1/2 transform -translate-x-1/2 text-white animate-bounce">
        <div class="w-6 h-10 border-2 border-white rounded-full flex justify-center">
          <div class="w-1 h-3 bg-white rounded-full mt-2 animate-pulse"></div>
        </div>
      </div>
    </section>

    <!-- Stats Section -->
    <section class="py-20 bg-gray-50 dark:bg-gray-800">
      <div class="max-w-6xl mx-auto px-6">
        <div class="grid grid-cols-2 md:grid-cols-4 gap-8">
          <div v-for="stat in stats" :key="stat.label" 
               class="text-center group hover:scale-105 transition-transform duration-300">
            <div class="text-4xl mb-2">{{ stat.icon }}</div>
            <div class="text-3xl md:text-4xl font-bold text-green-600 dark:text-green-400 mb-2">
              {{ stat.number }}
            </div>
            <div class="text-gray-600 dark:text-gray-300 font-medium">{{ stat.label }}</div>
          </div>
        </div>
      </div>
    </section>

    <main class="max-w-7xl mx-auto px-6 space-y-32 py-20">

      <!-- Sobre Nosotros con diseño moderno -->
      <section id="sobre-nosotros" class="relative">
        <div class="text-center mb-16">
          <h2 class="text-5xl font-bold mb-6 bg-gradient-to-r from-green-600 to-blue-600 bg-clip-text text-transparent">
            Nuestra Propuesta
          </h2>
          <div class="w-24 h-1 bg-gradient-to-r from-green-500 to-blue-500 mx-auto"></div>
        </div>
        
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center">
          <!-- Misión -->
          <div class="group">
            <div class="bg-white dark:bg-gray-800 p-8 rounded-3xl shadow-2xl hover:shadow-3xl transition-all duration-500 transform hover:-translate-y-2 border border-green-100 dark:border-green-900">
              <div class="flex items-center mb-6">
                <div class="w-16 h-16 bg-gradient-to-r from-green-500 to-green-600 rounded-2xl flex items-center justify-center text-white text-2xl font-bold mr-4">
                  M
                </div>
                <h3 class="text-3xl font-bold text-green-700 dark:text-green-300">Nuestra Misión</h3>
              </div>
              <p class="text-lg leading-relaxed text-gray-700 dark:text-gray-300">{{ mission }}</p>
              <div class="mt-6 flex flex-wrap gap-2">
                <span class="px-3 py-1 bg-green-100 dark:bg-green-900 text-green-800 dark:text-green-200 rounded-full text-sm font-medium">Innovación</span>
                <span class="px-3 py-1 bg-blue-100 dark:bg-blue-900 text-blue-800 dark:text-blue-200 rounded-full text-sm font-medium">Precisión</span>
                <span class="px-3 py-1 bg-purple-100 dark:bg-purple-900 text-purple-800 dark:text-purple-200 rounded-full text-sm font-medium">Eficiencia</span>
              </div>
            </div>
          </div>
          
          <!-- Visión -->
          <div class="group">
            <div class="bg-white dark:bg-gray-800 p-8 rounded-3xl shadow-2xl hover:shadow-3xl transition-all duration-500 transform hover:-translate-y-2 border border-blue-100 dark:border-blue-900">
              <div class="flex items-center mb-6">
                <div class="w-16 h-16 bg-gradient-to-r from-blue-500 to-blue-600 rounded-2xl flex items-center justify-center text-white text-2xl font-bold mr-4">
                  V
                </div>
                <h3 class="text-3xl font-bold text-blue-700 dark:text-blue-300">Nuestra Visión</h3>
              </div>
              <p class="text-lg leading-relaxed text-gray-700 dark:text-gray-300">{{ vision }}</p>
              <div class="mt-6 flex flex-wrap gap-2">
                <span class="px-3 py-1 bg-blue-100 dark:bg-blue-900 text-blue-800 dark:text-blue-200 rounded-full text-sm font-medium">Liderazgo</span>
                <span class="px-3 py-1 bg-green-100 dark:bg-green-900 text-green-800 dark:text-green-200 rounded-full text-sm font-medium">Sostenibilidad</span>
                <span class="px-3 py-1 bg-purple-100 dark:bg-purple-900 text-purple-800 dark:text-purple-200 rounded-full text-sm font-medium">Transformación</span>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Servicios con Cards Modernas -->
      <section id="servicios" class="relative">
        <div class="text-center mb-20">
          <h2 class="text-5xl font-bold mb-6 bg-gradient-to-r from-green-600 to-blue-600 bg-clip-text text-transparent">
            Áreas de Aplicación
          </h2>
          <p class="text-xl text-gray-600 dark:text-gray-300 max-w-3xl mx-auto">
            Soluciones especializadas para cada industria con tecnología de vanguardia
          </p>
          <div class="w-24 h-1 bg-gradient-to-r from-green-500 to-blue-500 mx-auto mt-6"></div>
        </div>
        
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <article v-for="(section, index) in sections" :key="section.id"
                   class="group relative bg-white dark:bg-gray-900 rounded-3xl overflow-hidden shadow-2xl hover:shadow-3xl transition-all duration-500 transform hover:-translate-y-4 border border-gray-100 dark:border-gray-800">
            
            <!-- Imagen con overlay -->
            <div class="relative h-64 overflow-hidden">
              <img :src="section.image" :alt="section.title" 
                   class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-700" 
                   loading="lazy" />
              <div class="absolute inset-0 bg-gradient-to-t from-black/60 via-black/20 to-transparent"></div>
              <div class="absolute top-4 right-4 text-4xl">{{ section.icon }}</div>
              <div class="absolute bottom-4 left-4 text-white">
                <h3 class="text-2xl font-bold mb-2">{{ section.title }}</h3>
              </div>
            </div>
            
            <!-- Contenido -->
            <div class="p-8">
              <p class="text-gray-700 dark:text-gray-300 leading-relaxed mb-6">
                {{ section.description }}
              </p>
              
              <!-- Features -->
              <div class="space-y-3">
                <h4 class="font-semibold text-gray-900 dark:text-white mb-3">Características principales:</h4>
                <ul class="space-y-2">
                  <li v-for="feature in section.features" :key="feature"
                      class="flex items-center text-sm text-gray-600 dark:text-gray-400">
                    <div class="w-2 h-2 bg-green-500 rounded-full mr-3"></div>
                    {{ feature }}
                  </li>
                </ul>
              </div>
              
              <!-- CTA Button -->
              <div class="mt-6 pt-6 border-t border-gray-200 dark:border-gray-700">
                <button class="w-full bg-gradient-to-r from-green-500 to-blue-500 text-white py-3 rounded-xl font-semibold hover:from-green-600 hover:to-blue-600 transition-all duration-300 transform hover:scale-105">
                  Saber Más
                </button>
              </div>
            </div>
          </article>
        </div>
      </section>

      <!-- Contacto Moderno -->
      <section id="contacto" class="relative">
        <div class="text-center mb-16">
          <h2 class="text-5xl font-bold mb-6 bg-gradient-to-r from-green-600 to-blue-600 bg-clip-text text-transparent">
            ¿Listo para Innovar?
          </h2>
          <p class="text-xl text-gray-600 dark:text-gray-300">
            Conversemos sobre cómo podemos transformar tu operación
          </p>
        </div>

        <div class="max-w-4xl mx-auto">
          <div class="bg-white dark:bg-gray-800 rounded-3xl shadow-2xl overflow-hidden border border-gray-100 dark:border-gray-800">
            <div class="grid grid-cols-1 lg:grid-cols-2">
              
              <!-- Información de contacto -->
              <div class="bg-gradient-to-br from-green-600 to-blue-600 p-12 text-white">
                <h3 class="text-3xl font-bold mb-8">Hablemos</h3>
                <div class="space-y-6">
                  <div class="flex items-center space-x-4">
                    <div class="w-12 h-12 bg-white/20 rounded-xl flex items-center justify-center">
                      📧
                    </div>
                    <div>
                      <p class="font-semibold">Email</p>
                      <p class="text-white/80">Freddy_andres@hotmail.es</p>
                    </div>
                  </div>
                  <div class="flex items-center space-x-4">
                    <div class="w-12 h-12 bg-white/20 rounded-xl flex items-center justify-center">
                      🌐
                    </div>
                    <div>
                      <p class="font-semibold">Plataforma</p>
                      <p class="text-white/80">app.telesens.cl</p>
                    </div>
                  </div>
                  <div class="flex items-center space-x-4">
                    <div class="w-12 h-12 bg-white/20 rounded-xl flex items-center justify-center">
                      🚀
                    </div>
                    <div>
                      <p class="font-semibold">Respuesta</p>
                      <p class="text-white/80">En menos de 24 horas</p>
                    </div>
                  </div>
                </div>
              </div>
              
              <!-- Formulario -->
              <div class="p-12">
                <form action="mailto:Freddy_andres@hotmail.es" method="POST" class="space-y-6" enctype="text/plain">
                  <div>
                    <input type="text" name="Nombre" placeholder="Tu nombre" required
                           class="w-full p-4 rounded-xl border border-gray-300 dark:border-gray-600 bg-white dark:bg-gray-700 text-gray-900 dark:text-white focus:outline-none focus:ring-2 focus:ring-green-500 focus:border-transparent transition-all duration-300" />
                  </div>
                  <div>
                    <input type="text" name="Asunto" placeholder="Asunto del mensaje" required
                           class="w-full p-4 rounded-xl border border-gray-300 dark:border-gray-600 bg-white dark:bg-gray-700 text-gray-900 dark:text-white focus:outline-none focus:ring-2 focus:ring-green-500 focus:border-transparent transition-all duration-300" />
                  </div>
                  <div>
                    <textarea name="Mensaje" placeholder="Cuéntanos sobre tu proyecto..." rows="5" required
                              class="w-full p-4 rounded-xl border border-gray-300 dark:border-gray-600 bg-white dark:bg-gray-700 text-gray-900 dark:text-white focus:outline-none focus:ring-2 focus:ring-green-500 focus:border-transparent resize-none transition-all duration-300"></textarea>
                  </div>
                  <button type="submit"
                          class="w-full bg-gradient-to-r from-green-600 to-blue-600 hover:from-green-700 hover:to-blue-700 text-white py-4 rounded-xl font-bold transition-all duration-300 transform hover:scale-105 shadow-lg hover:shadow-xl">
                    Enviar Mensaje
                  </button>
                </form>
              </div>
            </div>
          </div>
        </div>
      </section>
      
    </main>
  </div>
</template>