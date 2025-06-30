<script setup lang="ts">
import { ref, onMounted } from 'vue';

// SEO y meta tags
useHead({
  title: 'Telesens Chile - Telemetría Inteligente para el Futuro',
  meta: [
    { name: 'description', content: 'Soluciones innovadoras de monitoreo y análisis de datos mediante telemetría inteligente para agricultura, psicultura e industria.' },
    { name: 'keywords', content: 'telemetría, monitoreo, IoT, agricultura inteligente, psicultura, sensores, Chile' }
  ]
});

const mission = ref(`Proveer soluciones avanzadas de monitoreo y análisis de datos mediante telemetría inteligente, potenciando decisiones precisas en sectores productivos como la agricultura, psicultura, industria y medio ambiente.`);
const vision = ref(`Ser referentes en innovación tecnológica para monitoreo en tiempo real, liderando la transformación digital en Chile con soluciones eficientes, seguras y sostenibles.`);

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
    description: 'Maximiza tu productividad con monitoreo en tiempo real de cultivos, optimización de recursos hídricos y alertas predictivas.',
    image: 'https://res-console.cloudinary.com/dobkjiqyn/thumbnails/v1/image/upload/v1744161059/bG9nb19sZXRyYXNfd2ViX3RrMndseQ==/drilldown',
    icon: '🌱',
    features: ['Sensores de humedad del suelo', 'Estaciones meteorológicas', 'Monitoreo inteligente 24/7'],
    color: 'from-green-500 to-emerald-600'
  },
  {
    id: 'psicultura',
    title: 'Psicultura de Precisión',
    description: 'Protege tu inversión con control continuo de parámetros críticos del agua y alertas inmediatas ante cambios peligrosos.',
    image: '/img/psicultura.jpg',
    icon: '🐟',
    features: ['Monitoreo de oxígeno disuelto', 'Control de temperatura', 'Alertas de emergencia 24/7'],
    color: 'from-blue-500 to-cyan-600'
  },
  {
    id: 'industria',
    title: 'Industria 4.0',
    description: 'Optimiza procesos industriales con monitoreo predictivo, control de calidad automatizado y trazabilidad completa.',
    image: '/img/industria.jpg',
    icon: '🏭',
    features: ['Monitoreo de temperatura', 'Control de procesos', 'Reportes automáticos'],
    color: 'from-purple-500 to-indigo-600'
  },
];

// Stats más realistas para startup
const stats = [
  { number: '2024', label: 'Año de Fundación', icon: '🚀', description: 'Empresa innovadora chilena' },
  { number: '3', label: 'Sectores Clave', icon: '🎯', description: 'Agricultura, Psicultura, Industria' },
  { number: '24/7', label: 'Soporte Técnico', icon: '🔧', description: 'Atención personalizada' },
  { number: '100%', label: 'Soluciones Personalizadas', icon: '⚡', description: 'Adaptadas a tu negocio' }
];

const benefits = [
  {
    title: 'Implementación Rápida',
    description: 'Instalación y configuración en menos de 24 horas',
    icon: '⚡',
    color: 'bg-yellow-500'
  },
  {
    title: 'Sin Inversión Inicial',
    description: 'Modelo de suscripción flexible sin costos de entrada',
    icon: '💰',
    color: 'bg-green-500'
  },
  {
    title: 'Soporte Local',
    description: 'Equipo técnico chileno disponible cuando lo necesites',
    icon: '🇨🇱',
    color: 'bg-blue-500'
  },
  {
    title: 'Tecnología Probada',
    description: 'Soluciones basadas en estándares internacionales',
    icon: '🔬',
    color: 'bg-purple-500'
  }
];
</script>

<template>
  <div class="min-h-screen font-sans2 bg-white dark:bg-gray-900 text-gray-800 dark:text-white overflow-hidden">
    
    <!-- Hero Section Modernizado -->
    <section id="inicio" class="relative min-h-screen flex items-center justify-center overflow-hidden">
      <!-- Fondo con mesh gradient moderno -->
      <div class="absolute inset-0">
        <div class="absolute inset-0 bg-gradient-to-br from-emerald-400 via-blue-500 to-purple-600 dark:from-emerald-600 dark:via-blue-700 dark:to-purple-800"></div>
        <div class="absolute inset-0 bg-[url('data:image/svg+xml,%3Csvg%20width%3D%2260%22%20height%3D%2260%22%20viewBox%3D%220%200%2060%2060%22%20xmlns%3D%22http%3A//www.w3.org/2000/svg%22%3E%3Cg%20fill%3D%22none%22%20fill-rule%3D%22evenodd%22%3E%3Cg%20fill%3D%22%23ffffff%22%20fill-opacity%3D%220.05%22%3E%3Ccircle%20cx%3D%2230%22%20cy%3D%2230%22%20r%3D%222%22/%3E%3C/g%3E%3C/g%3E%3C/svg%3E')] opacity-20"></div>
        
        <!-- Elementos flotantes modernos -->
        <div class="absolute top-20 left-10 w-32 h-32 bg-white/10 rounded-full blur-xl animate-pulse"></div>
        <div class="absolute bottom-20 right-20 w-48 h-48 bg-emerald-300/20 rounded-full blur-2xl animate-float"></div>
        <div class="absolute top-1/2 left-1/4 w-24 h-24 bg-blue-300/20 rounded-full blur-lg animate-ping" style="animation-duration: 2s;"></div>
      </div>
      
      <!-- Contenido del Hero -->
      <div class="relative z-10 text-center space-y-8 px-6 max-w-6xl mx-auto" 
           :class="isVisible ? 'animate-fade-in-up' : 'opacity-0'">
        <div class="space-y-6">
          <div class="inline-flex items-center px-4 py-2 bg-white/20 backdrop-blur-lg rounded-full text-white/90 text-sm font-medium mb-4">
            🚀 Nueva empresa chilena de tecnología
          </div>
          
          <h1 class="text-5xl md:text-7xl font-black text-white leading-tight">
            <span class="bg-gradient-to-r from-emerald-300 via-blue-300 to-purple-300 bg-clip-text text-transparent">
              El futuro del
            </span>
            <br>
            <span class="text-white text-shadow">monitoreo inteligente</span>
          </h1>
          
          <p class="text-xl md:text-2xl text-white/90 font-light max-w-4xl mx-auto leading-relaxed">
            Soluciones de <strong class="text-emerald-300">telemetría personalizadas</strong> 
            para empresas que buscan <strong class="text-blue-300">innovar y crecer</strong> en Chile
          </p>
        </div>
        
        <div class="flex flex-col sm:flex-row gap-4 justify-center items-center pt-8">
          <a href="https://app.telesens.cl"
             class="group bg-white text-gray-900 px-8 py-4 rounded-full text-lg font-bold hover:bg-emerald-50 transition-all duration-300 transform hover:scale-105 shadow-2xl">
            <span class="flex items-center gap-2">
              Conoce nuestra plataforma
              <span class="group-hover:translate-x-1 transition-transform">→</span>
            </span>
          </a>
          <a href="#beneficios"
             class="border-2 border-white text-white px-8 py-4 rounded-full text-lg font-bold hover:bg-white hover:text-gray-900 transition-all duration-300 transform hover:scale-105">
            ¿Por qué Telesens?
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

    <!-- Stats Section Actualizada -->
    <section class="py-20 bg-gradient-to-r from-gray-50 to-gray-100 dark:from-gray-800 dark:to-gray-900">
      <div class="max-w-6xl mx-auto px-6">
        <div class="text-center mb-12">
          <h2 class="text-3xl font-bold text-gray-900 dark:text-white mb-4">
            Conoce a Telesens Chile
          </h2>
          <p class="text-lg text-gray-600 dark:text-gray-300">
            Una startup chilena comprometida con la innovación tecnológica
          </p>
        </div>
        
        <div class="grid grid-cols-2 md:grid-cols-4 gap-8">
          <div v-for="stat in stats" :key="stat.label" 
               class="text-center group hover:scale-105 transition-all duration-300 bg-white dark:bg-gray-800 p-6 rounded-2xl shadow-lg">
            <div class="text-4xl mb-3">{{ stat.icon }}</div>
            <div class="text-2xl md:text-3xl font-bold text-emerald-600 dark:text-emerald-400 mb-2">
              {{ stat.number }}
            </div>
            <div class="text-gray-900 dark:text-white font-semibold mb-1">{{ stat.label }}</div>
            <div class="text-sm text-gray-600 dark:text-gray-400">{{ stat.description }}</div>
          </div>
        </div>
      </div>
    </section>

    <main class="max-w-7xl mx-auto px-6 space-y-32 py-20">

      <!-- Beneficios Section -->
      <section id="beneficios" class="relative">
        <div class="text-center mb-16">
          <h2 class="text-4xl md:text-5xl font-bold mb-6 bg-gradient-to-r from-emerald-600 to-blue-600 bg-clip-text text-transparent">
            ¿Por qué elegir Telesens?
          </h2>
          <p class="text-xl text-gray-600 dark:text-gray-300 max-w-3xl mx-auto">
            Como startup, entendemos las necesidades de empresas que buscan crecer con tecnología accesible
          </p>
          <div class="w-24 h-1 bg-gradient-to-r from-emerald-500 to-blue-500 mx-auto mt-6"></div>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
          <div v-for="benefit in benefits" :key="benefit.title"
               class="text-center group hover:scale-105 transition-all duration-300">
            <div class="relative mb-6">
              <div :class="[benefit.color, 'w-16 h-16 rounded-2xl flex items-center justify-center text-white text-2xl mx-auto shadow-lg group-hover:shadow-xl transition-shadow duration-300']">
                {{ benefit.icon }}
              </div>
            </div>
            <h3 class="text-xl font-bold text-gray-900 dark:text-white mb-3">
              {{ benefit.title }}
            </h3>
            <p class="text-gray-600 dark:text-gray-300 leading-relaxed">
              {{ benefit.description }}
            </p>
          </div>
        </div>
      </section>

      <!-- Sobre Nosotros Modernizado -->
      <section id="sobre-nosotros" class="relative">
        <div class="text-center mb-16">
          <h2 class="text-4xl md:text-5xl font-bold mb-6 bg-gradient-to-r from-emerald-600 to-blue-600 bg-clip-text text-transparent">
            Nuestra Propuesta
          </h2>
          <div class="w-24 h-1 bg-gradient-to-r from-emerald-500 to-blue-500 mx-auto"></div>
        </div>
        
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center">
          <!-- Misión -->
          <div class="group">
            <div class="bg-white dark:bg-gray-800 p-8 rounded-3xl shadow-2xl hover:shadow-3xl transition-all duration-500 transform hover:-translate-y-2 border border-emerald-100 dark:border-emerald-900">
              <div class="flex items-center mb-6">
                <div class="w-16 h-16 bg-gradient-to-r from-emerald-500 to-emerald-600 rounded-2xl flex items-center justify-center text-white text-2xl font-bold mr-4">
                  🎯
                </div>
                <h3 class="text-3xl font-bold text-emerald-700 dark:text-emerald-300">Nuestra Misión</h3>
              </div>
              <p class="text-lg leading-relaxed text-gray-700 dark:text-gray-300">{{ mission }}</p>
              <div class="mt-6 flex flex-wrap gap-2">
                <span class="px-3 py-1 bg-emerald-100 dark:bg-emerald-900 text-emerald-800 dark:text-emerald-200 rounded-full text-sm font-medium">Precisión</span>
                <span class="px-3 py-1 bg-blue-100 dark:bg-blue-900 text-blue-800 dark:text-blue-200 rounded-full text-sm font-medium">Eficiencia</span>
                <span class="px-3 py-1 bg-purple-100 dark:bg-purple-900 text-purple-800 dark:text-purple-200 rounded-full text-sm font-medium">Escalabilidad</span>
              </div>
            </div>
          </div>
          
          <!-- Visión -->
          <div class="group">
            <div class="bg-white dark:bg-gray-800 p-8 rounded-3xl shadow-2xl hover:shadow-3xl transition-all duration-500 transform hover:-translate-y-2 border border-blue-100 dark:border-blue-900">
              <div class="flex items-center mb-6">
                <div class="w-16 h-16 bg-gradient-to-r from-blue-500 to-blue-600 rounded-2xl flex items-center justify-center text-white text-2xl font-bold mr-4">
                  🚀
                </div>
                <h3 class="text-3xl font-bold text-blue-700 dark:text-blue-300">Nuestra Visión</h3>
              </div>
              <p class="text-lg leading-relaxed text-gray-700 dark:text-gray-300">{{ vision }}</p>
              <div class="mt-6 flex flex-wrap gap-2">
                <span class="px-3 py-1 bg-blue-100 dark:bg-blue-900 text-blue-800 dark:text-blue-200 rounded-full text-sm font-medium">Liderazgo Regional</span>
                <span class="px-3 py-1 bg-emerald-100 dark:bg-emerald-900 text-emerald-800 dark:text-emerald-200 rounded-full text-sm font-medium">Innovación</span>
                <span class="px-3 py-1 bg-purple-100 dark:bg-purple-900 text-purple-800 dark:text-purple-200 rounded-full text-sm font-medium">Transformación</span>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Servicios Mejorados -->
      <section id="servicios" class="relative">
        <div class="text-center mb-20">
          <h2 class="text-4xl md:text-5xl font-bold mb-6 bg-gradient-to-r from-emerald-600 to-blue-600 bg-clip-text text-transparent">
            Soluciones Especializadas
          </h2>
          <p class="text-xl text-gray-600 dark:text-gray-300 max-w-3xl mx-auto">
            Tecnología adaptada a las necesidades específicas de cada industria
          </p>
          <div class="w-24 h-1 bg-gradient-to-r from-emerald-500 to-blue-500 mx-auto mt-6"></div>
        </div>
        
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <article v-for="(section, index) in sections" :key="section.id"
                   class="group relative bg-white dark:bg-gray-900 rounded-3xl overflow-hidden shadow-2xl hover:shadow-3xl transition-all duration-500 transform hover:-translate-y-4 border border-gray-100 dark:border-gray-800">
            
            <!-- Header con gradiente -->
            <div :class="[`bg-gradient-to-r ${section.color}`, 'p-6 text-white']">
              <div class="flex items-center justify-between mb-4">
                <div class="text-4xl">{{ section.icon }}</div>
                <div class="w-12 h-12 bg-white/20 rounded-full flex items-center justify-center">
                  <div class="w-6 h-6 bg-white rounded-full"></div>
                </div>
              </div>
              <h3 class="text-2xl font-bold">{{ section.title }}</h3>
            </div>
            
            <!-- Contenido -->
            <div class="p-8">
              <p class="text-gray-700 dark:text-gray-300 leading-relaxed mb-6">
                {{ section.description }}
              </p>
              
              <!-- Features -->
              <div class="space-y-3 mb-6">
                <h4 class="font-semibold text-gray-900 dark:text-white mb-3">✨ Incluye:</h4>
                <ul class="space-y-2">
                  <li v-for="feature in section.features" :key="feature"
                      class="flex items-center text-sm text-gray-600 dark:text-gray-400">
                    <div class="w-2 h-2 bg-emerald-500 rounded-full mr-3 flex-shrink-0"></div>
                    {{ feature }}
                  </li>
                </ul>
              </div>
              
              <!-- CTA Button -->
              <button :class="[`bg-gradient-to-r ${section.color}`, 'w-full text-white py-3 rounded-xl font-semibold hover:opacity-90 transition-all duration-300 transform hover:scale-105']">
                Saber Más
              </button>
            </div>
          </article>
        </div>
      </section>

      <!-- Contacto Modernizado -->
      <section id="contacto" class="relative">
        <div class="text-center mb-16">
          <h2 class="text-4xl md:text-5xl font-bold mb-6 bg-gradient-to-r from-emerald-600 to-blue-600 bg-clip-text text-transparent">
            ¿Hablamos de tu proyecto?
          </h2>
          <p class="text-xl text-gray-600 dark:text-gray-300">
            Como startup, valoramos cada conversación. Hablemos sin compromiso.
          </p>
        </div>

        <div class="max-w-5xl mx-auto">
          <div class="bg-white dark:bg-gray-800 rounded-3xl shadow-2xl overflow-hidden border border-gray-100 dark:border-gray-800">
            <div class="grid grid-cols-1 lg:grid-cols-2">
              
              <!-- Información de contacto -->
              <div class="bg-gradient-to-br from-emerald-600 to-blue-600 p-12 text-white">
                <h3 class="text-3xl font-bold mb-8">Conectemos</h3>
                <div class="space-y-6">
                  <div class="flex items-center space-x-4">
                    <div class="w-12 h-12 bg-white/20 rounded-xl flex items-center justify-center">
                      📧
                    </div>
                    <div>
                      <p class="font-semibold">Email directo</p>
                      <p class="text-white/80">Contacto@telesens.cl</p>
                    </div>
                  </div>
                  <div class="flex items-center space-x-4">
                    <div class="w-12 h-12 bg-white/20 rounded-xl flex items-center justify-center">
                      🌐
                    </div>
                    <div>
                      <p class="font-semibold">Plataforma</p>
                      <p class="text-white/80">www.telesens.cl</p>
                    </div>
                  </div>
                  <div class="flex items-center space-x-4">
                    <div class="w-12 h-12 bg-white/20 rounded-xl flex items-center justify-center">
                      ⚡
                    </div>
                    <div>
                      <p class="font-semibold">Respuesta rápida</p>
                      <p class="text-white/80">Menos de 24 horas</p>
                    </div>
                  </div>
                  <div class="flex items-center space-x-4">
                    <div class="w-12 h-12 bg-white/20 rounded-xl flex items-center justify-center">
                      🇨🇱
                    </div>
                    <div>
                      <p class="font-semibold">Empresa chilena</p>
                      <p class="text-white/80">Soporte local garantizado</p>
                    </div>
                  </div>
                </div>
              </div>
              
              <!-- Formulario -->
              <div class="p-12">
                <form action="mailto:Freddy_andres@hotmail.es" method="POST" class="space-y-6" enctype="text/plain">
                  <div>
                    <label class="block text-sm font-medium text-gray-700 dark:text-gray-300 mb-2">
                      Nombre *
                    </label>
                    <input type="text" name="Nombre" placeholder="Tu nombre completo" required
                           class="w-full p-4 rounded-xl border border-gray-300 dark:border-gray-600 bg-white dark:bg-gray-700 text-gray-900 dark:text-white focus:outline-none focus:ring-2 focus:ring-emerald-500 focus:border-transparent transition-all duration-300" />
                  </div>
                  <div>
                    <label class="block text-sm font-medium text-gray-700 dark:text-gray-300 mb-2">
                      Empresa / Sector
                    </label>
                    <input type="text" name="Empresa" placeholder="¿A qué te dedicas?"
                           class="w-full p-4 rounded-xl border border-gray-300 dark:border-gray-600 bg-white dark:bg-gray-700 text-gray-900 dark:text-white focus:outline-none focus:ring-2 focus:ring-emerald-500 focus:border-transparent transition-all duration-300" />
                  </div>
                  <div>
                    <label class="block text-sm font-medium text-gray-700 dark:text-gray-300 mb-2">
                      Mensaje *
                    </label>
                    <textarea name="Mensaje" placeholder="Cuéntanos sobre tu proyecto, necesidades o dudas..." rows="4" required
                              class="w-full p-4 rounded-xl border border-gray-300 dark:border-gray-600 bg-white dark:bg-gray-700 text-gray-900 dark:text-white focus:outline-none focus:ring-2 focus:ring-emerald-500 focus:border-transparent resize-none transition-all duration-300"></textarea>
                  </div>
                  <button type="submit"
                          class="w-full bg-gradient-to-r from-emerald-600 to-blue-600 hover:from-emerald-700 hover:to-blue-700 text-white py-4 rounded-xl font-bold transition-all duration-300 transform hover:scale-105 shadow-lg hover:shadow-xl">
                    Enviar Mensaje
                  </button>
                  <p class="text-sm text-gray-500 dark:text-gray-400 text-center">
                    Te responderemos en menos de 24 horas 🚀
                  </p>
                </form>
              </div>
            </div>
          </div>
        </div>
      </section>
      
    </main>
  </div>
</template>

<style scoped>
@keyframes float {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-20px); }
}

.animate-float {
  animation: float 6s ease-in-out infinite;
}
</style>