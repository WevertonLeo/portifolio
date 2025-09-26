<template>
  <section id="contact" class="w-full flex flex-col items-center py-16 gap-6">

    <!-- Título -->
    <h2 class="text-4xl font-bold text-blue-600 text-center">📬 Contato</h2>

    <!-- Links livres, lado a lado no desktop -->
    <div class="flex flex-col md:flex-row gap-4 md:gap-6 items-center">

      <a
        href="https://www.linkedin.com/in/weverton-leonardo/"
        target="_blank"
        class="flex items-center justify-center gap-2 bg-blue-600 text-white rounded-full px-6 py-3 text-sm font-bold hover:bg-blue-700 transition"
      >
        🔗 LinkedIn
      </a>

      <a
        href="https://github.com/WevertonLeo"
        target="_blank"
        class="flex items-center justify-center gap-2 bg-gray-800 text-white rounded-full px-6 py-3 text-sm font-bold hover:bg-gray-900 transition"
      >
        🔗 GitHub
      </a>

      <a
        href="mailto:wevertonardo17@gmail.com"
        class="flex items-center justify-center gap-2 bg-green-600 text-white rounded-full px-6 py-3 text-sm font-bold hover:bg-green-700 transition"
      >
        📧 Email
      </a>

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
