<script setup>
defineProps({
  id: {
    type: String,
    required: true
  }
})

const languages = ['C', 'C++', 'Java', 'TypeScript/JavaScript', 'GO', 'Python', 'PHP']
const frameworks = ['Angular', 'Symfony', 'Gin', 'Drupal', 'Vue3 (Nuxt)']
const otherSkills = ['Tech Lead', 'Project Management', 'Communication', 'CI/CD', 'Microservices', 'Building Devcontainer', 'Pro VSCode']

const skillSections = [
  { title: 'Languages', skills: languages, bgColor: 'bg-purple-100', textColor: 'text-purple-700' },
  { title: 'Frameworks', skills: frameworks, bgColor: 'bg-blue-100', textColor: 'text-blue-700' },
  { title: 'Other Skills', skills: otherSkills, bgColor: 'bg-green-100', textColor: 'text-green-700' }
]
</script>

<template>
  <section :id="id" class="py-20 bg-gradient-to-b from-gray-50 to-white">
    <div class="container mx-auto px-4">
      <h2 class="text-5xl font-bold mb-16 text-center text-gray-800">Skills</h2>
      <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 max-w-6xl mx-auto">
        <div v-for="section in skillSections" :key="section.title" class="space-y-4">
          <h3 class="text-2xl font-semibold text-center">{{ section.title }}</h3>
          <div class="flex flex-wrap gap-3 justify-center">
            <span
              v-for="skill in section.skills"
              :key="skill"
              :class="[section.bgColor, section.textColor, 'px-4 py-2 rounded-lg font-medium shadow-sm transition-transform hover:scale-105']"
            >
              {{ skill }}
            </span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
