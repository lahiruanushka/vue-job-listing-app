<script setup>
import logo from '@/assets/img/logo.png';
</script>

<template>
  <nav class="bg-white border-b border-gray-200">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex h-20 items-center justify-between">
        <!-- Logo -->
        <a class="flex items-center space-x-2" href="index.html">
          <img class="h-10 w-auto" :src="logo" alt="Vue Jobs" />
          <span class="hidden md:block text-gray-800 text-2xl font-bold">Jobs Finder</span>
        </a>
        <!-- Navigation Links -->
        <div class="md:flex md:items-center">
          <div class="flex space-x-4">
            <a href="/" class="text-gray-800 hover:bg-gray-100 rounded-md px-3 py-2 transition duration-300">Home</a>
            <a href="/jobs" class="text-gray-800 hover:bg-gray-100 rounded-md px-3 py-2 transition duration-300">Jobs</a>
            <a href="/jobs/add" class="text-gray-800 hover:bg-gray-100 rounded-md px-3 py-2 transition duration-300">Add Job</a>
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
