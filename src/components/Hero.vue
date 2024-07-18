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
  <section class="bg-blue-700 py-20 mb-8">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col items-center">
      <div class="text-center">
        <h1 class="text-5xl font-extrabold text-white sm:text-6xl md:text-7xl">
          {{ title || 'Focus on Your Career Growth' }}
        </h1>
        <p class="my-6 text-2xl text-blue-200 sm:text-3xl md:text-4xl">
          {{ subtitle || 'Find the job that fits your skills and needs' }}
        </p>
      </div>
    </div>
  </section>
</template>

<style scoped>
/* Custom CSS */
section {
  background: linear-gradient(135deg, #3b82f6, #60a5fa);
}

h1 {
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
}

p {
  text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.3);
}
</style>
