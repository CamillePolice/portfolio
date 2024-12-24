<script setup>
defineProps({
  id: {
    type: String,
    required: true
  }
})

const jobs = [
  {
    title: 'Consultant Engineer',
    company: 'ITLink',
    url: "https://www.itlink.fr/",
    period: 'September 2021 – Present',
    location: 'Rennes',
    responsibilities: [
      'Development of Angular/Symfony websites',
      'Embedded Vue3',
      'Web project architecture',
      'Creation of map files',
      'Management of microservices',
      'CI/CD management (Jenkins)',
      'Architectur',
      'Lead Dev'
    ]
  },
  {
    title: 'Entrepreneurship - FullStack Developer',
    company: 'Asheal',
    url: "https://www.linkedin.com/company/asheal/",
    period: 'October 2021 – Present',
    location: 'Rennes',
    responsibilities: [
      'Created an application to optimize medical consultations using DjangoRestFramework (Python) and Angular',
      'Redesigned the application with GinFramework (GO) and Vue3 (Nuxt)',
      'Created and maintained CI/CD (GitlabCI)',
      'Microservices management',
      'Automated production environment deployment with Terraform',
      'Project management, Lead Dev'
    ]
  },
  {
    title: 'Consultant Engineer',
    company: 'Open',
    url: "https://www.open.global/",
    period: 'June 2021 – July 2021',
    location: 'Rennes',
    responsibilities: [
      'Development of websites using the Drupal8 CMS',
      'Handling ticket backlog'
    ]
  },
  {
    title: 'Consultant Engineer',
    company: 'Open',
    url: "https://www.open.global/",
    period: 'September 2019 – July 2020',
    location: 'Rennes',
    responsibilities: [
      'Development of websites using the Drupal8 CMS',
    ]
  },
  {
    title: 'Consultant Engineer',
    company: 'Orange Labs',
    "url": "https://www.orange.com/en/home",
    period: '11 weeks',
    location: 'Rennes',
    responsibilities: [
      'Creation of an automatic documentation generation tool based on Sphinx for Python projects within the DIESE team',
    ]
  }
]
</script>

<template>
  <section :id="id" class="py-20 bg-gray-50">
    <div class="container mx-auto px-4">
      <h2 class="text-4xl font-bold mb-12 text-center">Experiences</h2>
      <div class="max-w-4xl mx-auto space-y-12">
        <div v-for="(job, index) in jobs" :key="index" class="bg-white p-6 rounded-lg shadow-sm">
          <div class="flex justify-between items-start mb-4">
            <div>
              <h3 class="text-xl font-semibold">{{ job.title }}</h3>
              <p class="text-purple-600">
                <a :href="job.url" target="_blank" class="hover:underline">{{ job.company }}</a>
              </p>
            </div>
            <div class="text-right">
              <p class="text-gray-600">{{ job.period }}</p>
              <p class="text-gray-600">{{ job.location }}</p>
            </div>
          </div>
          <ul class="list-disc list-inside space-y-2 text-gray-700">
            <li v-for="(responsibility, idx) in job.responsibilities" :key="idx">
              {{ responsibility }}
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>
