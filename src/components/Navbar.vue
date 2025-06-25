<script setup lang="ts">
import { ref, computed, onMounted } from 'vue'
import { vAutoAnimate } from '@formkit/auto-animate'
import { Sun, Moon } from '~/composables/useIcons'
import { useTheme } from '~/composables/useTheme'

const mounted = ref(false)
const { isDarkMode, toggleTheme } = useTheme()
const icon = computed(() => isDarkMode.value ? Moon : Sun)
const iconColorClass = computed(() => isDarkMode.value ? 'text-white' : 'text-black')

onMounted(() => {
  mounted.value = true
})
</script>

<template>
  <nav class="w-full h-20 px-6 md:px-12 flex items-center justify-between shadow-sm 
    backdrop-blur-lg relative z-30 border-b-2 border-[#4CAF50] bg-white/70 dark:bg-gray-900/70
    font-sans2 tracking-wide">
    
    <!-- Logo -->
    <div class="flex items-center h-full">
      <a href="#inicio" class="flex items-center h-full">
        <img 
          src="https://res.cloudinary.com/dobkjiqyn/image/upload/v1744161514/icono_web_wxpf7m.webp" 
          alt="Logo claro" 
          class="h-full object-contain drop-shadow-md dark:hidden" />
        <img 
          src="https://res.cloudinary.com/dobkjiqyn/image/upload/v1745279295/WAWAW_Mesa_de_trabajo_1_dg5svu.webp" 
          alt="Logo oscuro"
          class="h-full object-contain drop-shadow-md hidden dark:block" />
      </a>
    </div>

    <!-- Opciones centradas -->
    <ul class="hidden md:flex flex-1 justify-center space-x-12 text-neutral-800 dark:text-neutral-100 font-semibold">
      <li>
        <a href="#inicio" class="text-xl py-3 px-3 hover:text-green-600 dark:hover:text-green-400 transition">
          Inicio
        </a>
      </li>
      <li>
        <a href="#sobre-nosotros" class="text-xl py-3 px-3 hover:text-green-600 dark:hover:text-green-400 transition">
          Sobre Nosotros
        </a>
      </li>
      <li>
        <a href="#servicios" class="text-xl py-3 px-3 hover:text-green-600 dark:hover:text-green-400 transition">
          Servicios
        </a>
      </li>
      <li>
        <a href="#contacto" class="text-xl py-3 px-3 hover:text-green-600 dark:hover:text-green-400 transition">
          Contacto
        </a>
      </li>
    </ul>

    <!-- Botón y tema -->
    <div class="flex items-center space-x-6">
      <a
        href="https://app.telesens.cl"
        class="hidden md:inline-block bg-green-600 hover:bg-green-700 text-white text-xl px-8 py-3 rounded-full transition shadow font-semibold"
      >
        Ingresar
      </a>

      <div class="relative" v-auto-animate>
        <button
          v-if="mounted"
          @click="toggleTheme"
          aria-label="Cambiar tema"
          class="p-3 rounded-full hover:bg-[#388E3C]/20 transition"
        >
          <component :is="icon" class="w-6 h-6" :class="iconColorClass" />
        </button>
      </div>
    </div>
  </nav>
</template>
