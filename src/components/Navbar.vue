<script setup>
import logo from '@/assets/img/logo.png'
</script>

<template>
  <nav class="bg-blue-700 border-b border-blue-500">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex h-20 items-center justify-between">
        <!-- Logo -->
        <a class="flex items-center space-x-2" href="index.html">
          <img class="h-10 w-auto" :src="job-search" alt="Vue Jobs" />
          <span class="hidden md:block text-white text-2xl font-bold">Jobs Finder</span>
        </a>
        <!-- Navigation Links -->
        <div class="md:flex md:items-center">
          <div class="flex space-x-4">
            <a href="index.html" class="text-white bg-blue-900 hover:bg-blue-800 rounded-md px-3 py-2 transition duration-300">Home</a>
            <a href="jobs.html" class="text-white hover:bg-blue-800 rounded-md px-3 py-2 transition duration-300">Jobs</a>
            <a href="add-job.html" class="text-white hover:bg-blue-800 rounded-md px-3 py-2 transition duration-300">Add Job</a>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>

<style scoped>
/* Custom CSS */
.container {
  max-width: 1200px;
}

a {
  font-size: 1rem;
}

a:hover {
  transform: scale(1.05);
}
</style>
