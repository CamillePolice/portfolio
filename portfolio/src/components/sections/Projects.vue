<script setup>
defineProps({
  id: {
    type: String,
    required: true
  }
})

const projects = [
  {
    title: 'Asheal - Healthcare Platform',
    description: {
      overview: 'Full-stack healthcare platform optimizing medical consultations through dedicated patient and practitioner portals.',
      versions: [
        {
          title: 'First Version',
          frontend: {
            name: 'Angular',
            tech: 'TypeScript'
          },
          backend: {
            name: 'Django REST Framework',
            tech: 'Python'
          },
          features: [
            'Containerized with Docker',
            'Automated infrastructure deployment via Terraform'
          ]
        },
        {
          title: 'Second Version (In Development)',
          frontend: {
            name: 'Vue3/Nuxt',
            tech: 'TypeScript'
          },
          backend: {
            name: 'Gin Framework',
            tech: 'Golang'
          },
          features: [
            'Improved architecture based on v1 learnings',
            'Enhanced performance and scalability'
          ]
        }
      ]
    },
    technologies: ['Vue3', 'Go', 'TypeScript', 'Docker', 'Terraform', 'Devcontainer'],
    badge: 'Professional'
  },
  {
    title: 'National Flood Monitoring System',
    description: {
      overview: 'Developed at ITLink, National flood monitoring and alert system for France.',
      versions: [
        {
          title: 'Stack',
          frontend: {
            name: 'Angular',
            tech: 'TypeScript'
          },
          backend: {
            name: 'Symfony',
            tech: 'PHP'
          }
        }
      ],
      features: [
        'Aggregates regional flood forecasts into a consolidated national assessment',
        'Email notifications to government administrators',
        'Real-time updates to Vigicrues platform',
        'Streamlines flood risk communication between centers'
      ]
    },
    technologies: ['MapServer', 'Websocket (Real-time updates and Live chat)', 'Devcontainer', 'CI/CD (Jenkins then GitlabCI)', "Unit testing (70% coverage)"],
    badge: 'Professional'
  },
  {
    title: 'Vigicrues - Official Flood Warning Service',
    description: {
      overview: 'France\'s official flood warning service website (vigicrues.gouv.fr), operated by SCHAPI.',
      features: [
        'Real-time monitoring of flood risks across French rivers',
        'Color-coded alert system (green, yellow, orange, red)',
        'Interactive map visualization',
        'Public information dashboard'
      ]
    },
    technologies: ['Angular', 'Symfony'],
    badge: 'Professional'
  },
  {
    title: 'Transport Synoptic',
    description: {
      overview: 'Interactive horizontal synoptic display system for tracking public transport vehicles in real-time.',
      features: [
        'Real-time vehicle position tracking',
        'Horizontal scrolling synoptic view',
        'Interactive station markers',
        'Live status updates'
      ]
    },
    technologies: ['Vue3', 'TypeScript', 'WebSockets', 'Canvas drawning', 'Embedded Vue3'],
    badge: 'Professional'
  },
  {
    title: 'Music Player',
    description: {
      overview: 'A Spotify-inspired music player built with Vue3 and Nuxt.',
      features: [
        'Play/pause/stop functionality',
        'Interactive timeline slider',
        'Audio thumbnail display',
        'Modern and responsive UI',
        'State management for player controls'
      ]
    },
    technologies: ['Vue3', 'Nuxt', 'TypeScript', 'Tailwind', 'PrimeVue'],
    badge: 'Personal'
  },
  {
    title: 'YokaiNoMori - Chess Game',
    description: {
      overview: 'An Android implementation of YokaiNoMori, a simplified chess variant designed for children.',
      features: [
        'Intuitive touch-based game interface',
        'Simplified chess rules for children',
        'Interactive board visualization',
        'Player vs Player mode',
        'Move validation system'
      ]
    },
    technologies: ['Java', 'Android SDK', 'XML'],
    badge: 'Personal'
  },
  {
    title: 'Bomberman Like',
    description: {
      overview: 'A 3D Bomberman-like game built with C++ and Irrlicht engine.',
      features: [
        'Real-time 3D gameplay mechanics',
        'Player vs Player combat',
        'Destructible environment',
        'Power-up system',
        'Collision detection'
      ]
    },
    technologies: ['C++', 'Irrlicht', '3D Graphics'],
    badge: 'Personal'
  },
  {
    title: 'Secret Santa Organizer',
    description: {
      overview: 'Automated gift exchange organizer using Python and SMTP email system.',
      features: [
        'Random assignment algorithm',
        'Automated email notifications',
        'SMTP integration',
        'Duplicate prevention',
        'Configurable exclusion rules'
      ]
    },
    technologies: ['Python', 'SMTP', 'Email Automation'],
    badge: 'Personal'
  },
]
</script>

<template>
  <section :id="id" class="py-20 bg-gray-50">
    <div class="container mx-auto px-4">
      <h2 class="text-4xl font-bold mb-12 text-center">Projects</h2>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-5xl mx-auto">
        <div v-for="project in projects" :key="project.title"
          class="bg-white rounded-lg shadow-sm p-6 hover:shadow-md transition-shadow relative">
          <div
            class="absolute top-4 right-4 px-2 py-1 rounded text-sm"
            :class="{
              'bg-blue-100 text-blue-700': project.badge === 'Professional',
              'bg-purple-100 text-purple-700': project.badge === 'Personal'
            }"
          >
            {{ project.badge }}
          </div>

          <h3 class="text-xl font-semibold mb-3 text-gray-800 pr-24">{{ project.title }}</h3>
          <p class="text-gray-600 mb-4">{{ project.description.overview }}</p>

          <template v-if="project.description.versions">
            <div v-for="version in project.description.versions" :key="version.title" class="mb-6">
              <h4 class="font-medium text-gray-800 text-lg mb-3">{{ version.title }}</h4>
              <div class="bg-gray-50 p-4 rounded-lg mb-3">
                <div class="grid grid-cols-2 gap-4">
                  <div>
                    <div class="text-sm text-gray-500 mb-1">Frontend</div>
                    <div class="font-medium text-gray-800">{{ version.frontend.name }}</div>
                    <div class="text-sm text-gray-600">({{ version.frontend.tech }})</div>
                  </div>
                  <div>
                    <div class="text-sm text-gray-500 mb-1">Backend</div>
                    <div class="font-medium text-gray-800">{{ version.backend.name }}</div>
                    <div class="text-sm text-gray-600">({{ version.backend.tech }})</div>
                  </div>
                </div>
              </div>
              <ul class="list-disc list-inside text-gray-600 space-y-1 ml-2">
                <li v-for="feature in version.features" :key="feature">{{ feature }}</li>
              </ul>
            </div>
          </template>

          <template v-if="project.description.features">
            <ul class="list-disc list-inside mb-4 text-gray-600 space-y-2">
              <li v-for="feature in project.description.features" :key="feature">{{ feature }}</li>
            </ul>
          </template>

          <div class="flex flex-wrap gap-2 pt-2">
            <span v-for="tech in project.technologies" :key="tech"
              class="px-2 py-1 bg-blue-100 text-blue-700 rounded-full text-sm">
              {{ tech }}
            </span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
