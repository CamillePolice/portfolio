<script setup>
defineProps({
  id: {
    type: String,
    required: true
  }
})
</script>

<template>
  <section :id="id" class="py-20 bg-gray-50">
    <div class="container mx-auto px-4">
      <h2 class="text-4xl font-bold mb-12 text-center">Contact</h2>
      <div class="max-w-lg mx-auto bg-white rounded-lg shadow-sm p-8">
        <div class="space-y-6">
          <div class="flex items-center space-x-4">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-purple-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
            </svg>
            <a href="mailto:camillepolice@icloud.com" class="text-purple-600 hover:text-purple-800">
              camillepolice@icloud.com
            </a>
          </div>
          <div class="flex items-center space-x-4">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-purple-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
            </svg>
            <span>Cesson-Sévigné, 35051</span>
          </div>
          <div class="flex items-center space-x-4">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-purple-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4" />
            </svg>
            <div class="flex space-x-4">
              <a href="https://github.com/CamillePolice" target="_blank" class="text-purple-600 hover:text-purple-800">GitHub</a>
              <a href="https://gitlab.com/CamillePolice" target="_blank" class="text-purple-600 hover:text-purple-800">GitLab</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
