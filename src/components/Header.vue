<template>
  <header class="fixed top-0 left-0 w-full bg-white/90 backdrop-blur-md shadow-md z-50">
    <div class="max-w-6xl mx-auto flex items-center justify-between px-6 py-4">

      <!-- Label Portfólio -->
      <span class="text-2xl font-bold text-blue-600">Portfólio</span>

      <!-- Desktop menu (escondido no mobile) -->
      <nav class="hidden md:flex gap-8">
        <a href="#about" class="text-gray-700 hover:text-blue-600 font-medium transition">Sobre</a>
        <a href="#skills" class="text-gray-700 hover:text-blue-600 font-medium transition">Habilidades</a>
        <a href="#projects" class="text-gray-700 hover:text-blue-600 font-medium transition">Projetos</a>
        <a href="#contact" class="text-gray-700 hover:text-blue-600 font-medium transition">Contato</a>
      </nav>

      <!-- Botão menu mobile -->
      <div class="md:hidden relative">
        <button @click="toggleDropdown" class="flex items-center gap-2 px-3 py-2 border rounded-lg border-gray-300 bg-white">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-blue-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
              d="M4 6h16M4 12h16M4 18h16" />
          </svg>
        </button>

        <!-- Dropdown -->
        <transition name="fade">
          <ul v-if="isOpen" class="absolute right-0 mt-2 w-40 bg-white border border-gray-200 rounded-xl shadow-lg overflow-hidden">
            <li><a @click="closeDropdown" href="#about" class="block px-4 py-3 hover:bg-blue-600 hover:text-white transition">Sobre</a></li>
            <li><a @click="closeDropdown" href="#skills" class="block px-4 py-3 hover:bg-blue-600 hover:text-white transition">Habilidades</a></li>
            <li><a @click="closeDropdown" href="#projects" class="block px-4 py-3 hover:bg-blue-600 hover:text-white transition">Projetos</a></li>
            <li><a @click="closeDropdown" href="#contact" class="block px-4 py-3 hover:bg-blue-600 hover:text-white transition">Contato</a></li>
          </ul>
        </transition>
      </div>

    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue'

const isOpen = ref(false)

const toggleDropdown = () => {
  isOpen.value = !isOpen.value
}

const closeDropdown = () => {
  isOpen.value = false
}
</script>

<style scoped>
/* Animação de fade */
.fade-enter-active, .fade-leave-active { transition: opacity 0.3s ease; }
.fade-enter-from, .fade-leave-to { opacity: 0; }
</style>