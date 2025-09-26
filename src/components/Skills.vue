<template>
  <section id="skills" class="max-w-6xl mx-auto px-6 py-16 flex flex-col items-center gap-8">
    <h2 class="text-4xl font-bold mb-8 text-blue-600 text-center">💡 Habilidades</h2>

    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 w-full">
      <div
        v-for="(skill, index) in skills"
        :key="index"
        class="flex flex-col gap-3 bg-white border border-gray-200 rounded-2xl shadow-lg p-4 hover:shadow-xl transition transform hover:scale-105"
      >
        <div class="flex items-center gap-3">
          <div class="text-3xl" :class="skill.color">{{ skill.icon }}</div>
          <h3 class="font-bold text-lg text-gray-800">{{ skill.category }}</h3>
        </div>
        <div class="flex flex-wrap gap-2 mt-2">
          <span
            v-for="(item, i) in skill.items"
            :key="i"
            class="bg-gray-100 text-gray-800 font-bold px-2 py-1 rounded-full text-sm"
            :class="skill.bgColor"
          >
            {{ item }}
          </span>
        </div>
      </div>

    </div>
  </section>
</template>

<script setup>
const skills = [
  {
    category: 'Backend',
    icon: '🖥️',
    color: 'text-blue-600',
    bgColor: 'bg-blue-100 text-blue-700',
    items: ['PHP', 'Laravel']
  },
  {
    category: 'Frontend',
    icon: '🎨',
    color: 'text-green-500',
    bgColor: 'bg-green-100 text-green-700',
    items: ['Vue.js', 'jQuery', 'Bootstrap', 'Tailwind']
  },
  {
    category: 'Banco de Dados',
    icon: '💾',
    color: 'text-purple-600',
    bgColor: 'bg-purple-100 text-purple-700',
    items: ['MySQL', 'SQL Server']
  },
  {
    category: 'Sistemas',
    icon: '🐧',
    color: 'text-yellow-500',
    bgColor: 'bg-yellow-100 text-yellow-700',
    items: ['Git', 'GitLab', 'Windows', 'Linux', 'Docker']
  },
  {
    category: 'Programação',
    icon: '🧑‍💻',
    color: 'text-red-500',
    bgColor: 'bg-red-100 text-red-700',
    items: ['APIs REST', 'TDD', 'SOLID', 'Clean Code']
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