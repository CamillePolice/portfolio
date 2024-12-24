<script setup>
defineProps({
  id: {
    type: String,
    required: true
  }
})
</script>

<template>
  <section :id="id" class="py-20 bg-white">
    <div class="container mx-auto px-4">
      <h2 class="text-4xl font-bold mb-12 text-center">About Me</h2>
      <div class="max-w-3xl mx-auto">
        <p class="text-lg text-gray-700 mb-6">
          Passionate about cutting-edge technologies and quality-driven development, I thrive on creating robust
          solutions as a Full-Stack Developer. My expertise spans CI/CD pipelines with GitLab CI and Terraform, while my
          experience as a Lead Developer has honed my skills in TypeScript, Vue 3, Symfony and Angular. I take pride in writing
          comprehensive tests and implementing best practices across all projects.
        </p>
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8 mt-12">
          <div>
            <h3 class="text-xl font-semibold mb-4">Interests</h3>
            <ul class="space-y-3">
              <li class="flex items-center space-x-2">
                <span class="text-purple-600">🎾</span>
                <span>Tennis, currently 15/2 (previous ranked 5/6)</span>
              </li>
              <li class="flex items-center space-x-2">
                <span class="text-purple-600">🎮</span>
                <span>League of Legends player (Diamond rank since 2021) and competitor with team ATAT</span>
              </li>
              <li class="flex items-center space-x-2">
                <span class="text-purple-600">✈️</span>
                <span>Traveled to South Korea, Mexico, Cuba, Egypt, Germany, United States, Morocco, Bahamas, Cabo verde, Jamaïca, Viet-Nam, Italia, Scotland, England, Poland</span>
              </li>
            </ul>
          </div>
          <div>
            <h3 class="text-xl font-semibold mb-4">Languages</h3>
            <ul class="space-y-3">
              <li class="flex items-center justify-between">
                <span>English</span>
                <div class="flex space-x-1">
                  <span class="w-2 h-2 rounded-full bg-purple-600"></span>
                  <span class="w-2 h-2 rounded-full bg-purple-600"></span>
                  <span class="w-2 h-2 rounded-full bg-purple-600"></span>
                  <span class="w-2 h-2 rounded-full bg-purple-600"></span>
                  <span class="w-2 h-2 rounded-full bg-gray-300"></span>
                </div>
              </li>
              <li class="flex items-center justify-between">
                <span>German</span>
                <div class="flex space-x-1">
                  <span class="w-2 h-2 rounded-full bg-purple-600"></span>
                  <span class="w-2 h-2 rounded-full bg-purple-600"></span>
                  <span class="w-2 h-2 rounded-full bg-gray-300"></span>
                  <span class="w-2 h-2 rounded-full bg-gray-300"></span>
                  <span class="w-2 h-2 rounded-full bg-gray-300"></span>
                </div>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
