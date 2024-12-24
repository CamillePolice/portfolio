<script setup>
const props = defineProps({
  sections: {
    type: Array,
    required: true
  }
})
</script>

<template>
  <nav class="fixed left-4 top-1/2 transform -translate-y-1/2 z-40">
    <ul class="space-y-4">
      <li v-for="section in sections" :key="section">
        <a
          :href="`#${section}`"
          class="block w-3 h-3 rounded-full bg-purple-200 hover:bg-purple-600 transition-colors"
          :title="section.charAt(0).toUpperCase() + section.slice(1)"
        />
      </li>
    </ul>
  </nav>
</template>
