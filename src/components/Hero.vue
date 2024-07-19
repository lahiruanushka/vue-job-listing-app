<script setup>
import { defineProps } from 'vue';

defineProps({
  title: {
    type: String,
    default: '',
  },
  subtitle: {
    type: String,
    default: '',
  }
});
</script>

<template>
  <section class="bg-white py-20 mb-8">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col items-center">
      <div class="text-center">
        <h1 class="text-5xl font-extrabold text-gray-900 sm:text-6xl md:text-7xl">
          {{ title || 'Find Your Dream Job' }}
        </h1>
        <p class="my-6 text-2xl text-gray-700 sm:text-3xl md:text-4xl">
          {{ subtitle || 'Search for job listings that suit your career goals.' }}
        </p>
      </div>
    </div>
  </section>
</template>

<style scoped>
/* Custom CSS */
section {
  background: linear-gradient(135deg, #f9fafb, #f3f4f6);
}

h1 {
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
}

p {
  text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.1);
}
</style>
