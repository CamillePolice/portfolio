<template>
  <section :id="id" class="py-20 bg-gray-50">
    <div class="container mx-auto px-4">
      <h2 class="text-4xl font-bold mb-12 text-center">Projects</h2>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-5xl mx-auto">
        <div class="bg-white rounded-lg shadow-sm p-6">
          <h3 class="text-xl font-semibold mb-3">Asheal - Medical Consultation Platform</h3>
          <p class="text-gray-600 mb-4">
            A full-stack application optimizing medical consultations, featuring both patient and doctor interfaces.
          </p>
          <div class="flex flex-wrap gap-2 mb-4">
            <span class="px-2 py-1 bg-blue-100 text-blue-700 rounded-full text-sm">Vue3</span>
            <span class="px-2 py-1 bg-blue-100 text-blue-700 rounded-full text-sm">Go</span>
            <span class="px-2 py-1 bg-blue-100 text-blue-700 rounded-full text-sm">Microservices</span>
          </div>
        </div>

        <div class="bg-white rounded-lg shadow-sm p-6">
          <h3 class="text-xl font-semibold mb-3">Map File Generator</h3>
          <p class="text-gray-600 mb-4">
            Developed at ITLink, this tool automates the creation and management of complex map files.
          </p>
          <div class="flex flex-wrap gap-2 mb-4">
            <span class="px-2 py-1 bg-blue-100 text-blue-700 rounded-full text-sm">Angular</span>
            <span class="px-2 py-1 bg-blue-100 text-blue-700 rounded-full text-sm">Symfony</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
defineProps({
  id: {
    type: String,
    required: true
  }
})
</script>
