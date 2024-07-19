<script setup>
import JobListing from './JobListing.vue';
import jobData from '@/jobs.json';
import { ref, defineProps } from 'vue';

// Define props
const props = defineProps({
  limit: Number,
  showButton: {
    type: Boolean,
    default: false
  }
});

// Jobs data
const jobs = ref(jobData.jobs); // Access 'jobs' array within jobData
</script>

<template>
  <section class="bg-white rounded-xl shadow-md relative">
    <div class="container-xl lg:container mx-auto">
      <h2 class="text-3xl font-bold text-green-500 mb-6 text-center">
        Browse Jobs
      </h2>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4 p-4">
        <JobListing v-for="job in jobs.slice(0, props.limit || jobs.length)" :key="job.id" :job="job" />
      </div>
    </div>
  </section>

  <section v-if="props.showButton" class="m-auto max-w-lg my-10 px-6">
    <a
      href="/jobs"
      class="block bg-black text-white text-center py-4 px-6 rounded-xl hover:bg-gray-700"
    >
      View All Jobs
    </a>
  </section>
</template>

<style scoped>
/* Add scoped styles here */
</style>
