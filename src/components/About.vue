<template>
  <section id="about" class="max-w-6xl mx-auto px-6 py-24 flex flex-col items-center">

    <!-- Card -->
    <div class="bg-white border border-gray-200 rounded-3xl shadow-lg p-8 md:p-12 w-full flex flex-col gap-12">
      
      <!-- Nome e breve descrição -->
      <div class="text-center md:text-left flex flex-col md:flex-row items-center gap-10 w-full">
        <div class="flex-1">
          <h1 class="text-3xl md:text-4xl font-semibold text-gray-600 mb-2">Olá, eu sou o</h1>
          <h2 class="text-4xl md:text-5xl font-bold text-blue-600 mb-2">Weverton Leonardo</h2>
          <p class="text-gray-700 text-lg md:text-xl">Desenvolvedor Full Stack | PHP | Laravel | Vue JS</p>
        </div>

        <!-- Foto -->
        <div class="flex-shrink-0 w-48 h-48 md:w-64 md:h-64 rounded-full overflow-hidden border-4 border-blue-600 shadow-lg">
          <img src="@/assets/img02.jpeg" alt="Weverton Leonardo" class="w-full h-full object-cover">
        </div>
      </div>

      <!-- Descrição detalhada -->
      <div class="text-gray-700 md:text-lg leading-relaxed max-w-3xl text-center md:text-left">
        <p>
          Sou Desenvolvedor Full Stack, especializado em Laravel e Vue.js.  
          Possuo sólida experiência com bancos de dados relacionais, APIs REST, TDD e versionamento de código com Git e GitLab.  
          Adoto princípios de Clean Code e práticas eficientes para entregar soluções escaláveis e de alta qualidade.  
          Experiência com Docker e Linux para ambientes de desenvolvimento confiáveis. Estou sempre em busca de novos desafios e aprendizado contínuo.
        </p>
      </div>

    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
section {
  opacity: 0;
  transform: translateY(20px);
  animation: fadeInUp 0.6s forwards;
}

@keyframes fadeInUp {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
