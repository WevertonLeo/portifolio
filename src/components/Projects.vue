<template>
  <section id="projects" class="max-w-6xl mx-auto px-6 py-16 flex flex-col items-center gap-8">
    <h2 class="text-4xl font-bold mb-8 text-blue-600 text-center">🚀 Projetos</h2>

    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 w-full">
      <div
        v-for="(project, index) in projects"
        :key="index"
        class="flex flex-col gap-3 bg-white border border-gray-200 rounded-2xl shadow-lg p-4 hover:shadow-xl transition transform hover:scale-105"
      >
        <h3 class="font-bold text-lg text-gray-800">{{ project.name }}</h3>
        <p class="text-gray-700 text-sm md:text-base">{{ project.description }}</p>
        <a
          :href="project.link"
          target="_blank"
          class="mt-2 inline-block w-max bg-blue-600 text-white rounded-full px-4 py-2 text-sm font-semibold hover:bg-blue-700 transition"
        >
            🔗 GitHub
        </a>
      </div>
    </div>

  </section>
</template>

<script setup>
const projects = [
  {
    name: 'Rede Social MyPet',
    description: 'Desenvolvido para conectar pessoas, instituições e animais em situação de rua!',
    link: 'https://github.com/WevertonLeo/MyPet'
  },
  {
    name: 'Portfólio Vue.js',
    description: 'Este portfólio foi desenvolvido com Vue.js, Tailwind e hospedado na Vercel.',
    link: 'https://github.com/WevertonLeo/portifolio'
  },
  {
    name: 'API RESTful',
    description: 'Web service nativo desenvolvido com PHP e MySql',
    link: 'https://github.com/WevertonLeo/API'
  }
]
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