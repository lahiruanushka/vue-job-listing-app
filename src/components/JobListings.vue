<script setup>
import JobListing from './JobListing.vue';
import { reactive, defineProps, onMounted } from 'vue';
import { RouterLink } from 'vue-router';
import PulseLoader from 'vue-spinner/src/PulseLoader.vue'; // Ensure this path is correct
import axios from 'axios';

// Define props
const props = defineProps({
  limit: Number,
  showButton: {
    type: Boolean,
    default: false
  }
});

// Jobs data
const state = reactive({
  jobs: [],
  isLoading: true,
  error: null, // Add error state
});

onMounted(async () => {
  try {
    const response = await axios.get('/api/jobs'); // Adjust this if necessary
    state.jobs = response.data;  
  } catch (error) {
    state.error = 'Error fetching jobs. Please try again later.'; // Set error message
    console.error('Error fetching jobs.', error);
  } finally {
    state.isLoading = false;
  }
});
</script>


<template>
  <section class="bg-white rounded-xl shadow-md relative">
    <div class="container-xl lg:container mx-auto">
      <h2 class="text-3xl font-bold text-green-500 mb-6 text-center">
        Browse Jobs
      </h2>
      <!-- Show loading spinner -->
      <div v-if="state.isLoading" class="text-center text-gray-500 py-6">
        <PulseLoader />
      </div>

      <!-- Show Job listing -->
      <div v-else class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4 p-4">
        <JobListing v-for="job in state.jobs.slice(0, props.limit || state.jobs.length)" :key="job.id" :job="job" />
      </div>
    </div>
  </section>

  <section v-if="props.showButton" class="m-auto max-w-lg my-10 px-6">
    <RouterLink
      to="/jobs"
      class="block bg-black text-white text-center py-4 px-6 rounded-xl hover:bg-gray-700"
    >
      View All Jobs
    </RouterLink>
  </section>
</template>

<style scoped>
/* Add scoped styles here */
</style>
