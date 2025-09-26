<template>
  <div class="bg-white min-h-screen text-gray-900">
    <Header />
    <About />
    <Skills />
    <Projects />
    <Contact />
    
  </div>
</template>

<script setup>
import Header from './components/Header.vue'
import About from './components/About.vue'
import Skills from './components/Skills.vue'
import Projects from './components/Projects.vue'
import Contact from './components/Contact.vue'
</script>

<style>
/* Scroll suave */
html {
  scroll-behavior: smooth;
}

/* Padronização de fontes e cores */
body {
  font-family: 'Inter', sans-serif;
  background-color: #f9fafb; /* cinza claro */
}

/* Links padrão */
a {
  text-decoration: none;
}
</style>