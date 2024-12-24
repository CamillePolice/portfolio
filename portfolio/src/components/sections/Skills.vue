<script setup>
defineProps({
  id: {
    type: String,
    required: true
  }
})

const languages = ['C', 'C++', 'Java', 'TypeScript/JavaScript', 'GO', 'Python', 'PHP']
const frameworks = ['Angular', 'Symfony', 'Gin', 'Drupal', 'Vue3 (Nuxt)']
const otherSkills = ['Tech Lead', 'Project Management', 'Communication', 'CI/CD', 'Microservices']
</script>

<template>
  <section :id="id" class="py-20 bg-white">
    <div class="container mx-auto px-4">
      <h2 class="text-4xl font-bold mb-12 text-center">Skills</h2>
      <div class="max-w-4xl mx-auto">
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
          <div class="space-y-6">
            <h3 class="text-xl font-semibold mb-4">Languages</h3>
            <div class="flex flex-wrap gap-2">
              <span v-for="lang in languages" :key="lang"
                class="px-3 py-1 bg-purple-100 text-purple-700 rounded-full">
                {{ lang }}
              </span>
            </div>
          </div>

          <div class="space-y-6">
            <h3 class="text-xl font-semibold mb-4">Frameworks</h3>
            <div class="flex flex-wrap gap-2">
              <span v-for="framework in frameworks" :key="framework"
                class="px-3 py-1 bg-blue-100 text-blue-700 rounded-full">
                {{ framework }}
              </span>
            </div>
          </div>

          <div class="space-y-6">
            <h3 class="text-xl font-semibold mb-4">Other Skills</h3>
            <div class="flex flex-wrap gap-2">
              <span v-for="skill in otherSkills" :key="skill"
                class="px-3 py-1 bg-green-100 text-green-700 rounded-full">
                {{ skill }}
              </span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
