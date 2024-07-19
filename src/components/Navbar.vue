<script setup>
import { RouterLink, useRoute } from 'vue-router';
import logo from '@/assets/img/logo.png';

const route = useRoute();

const isActiveLink = (routePath) => {
  return route.path === routePath;
}
</script>

<template>
  <nav class="bg-white border-b border-gray-200">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex h-20 items-center justify-between">
        <!-- Logo -->
        <RouterLink class="flex items-center space-x-2" to="/">
          <img class="h-10 w-auto" :src="logo" alt="Vue Jobs" />
          <span class="hidden md:block text-gray-800 text-2xl font-bold">Jobs Finder</span>
        </RouterLink>
        <!-- Navigation Links -->
        <div class="md:flex md:items-center">
          <div class="flex space-x-4">
            <RouterLink 
              to="/" 
              :class="[
                isActiveLink('/') ? 'active' : 'text-gray-800', 
                'hover:bg-gray-100', 
                'rounded-md', 
                'px-3', 
                'py-2', 
                'transition duration-300'
              ]">Home
            </RouterLink>
            <RouterLink 
              to="/jobs" 
              :class="[
                isActiveLink('/jobs') ? 'active' : 'text-gray-800', 
                'hover:bg-gray-100', 
                'rounded-md', 
                'px-3', 
                'py-2', 
                'transition duration-300'
              ]">Jobs
            </RouterLink>
            <RouterLink 
              to="/jobs/add" 
              :class="[
                isActiveLink('/jobs/add') ? 'active' : 'text-gray-800', 
                'hover:bg-gray-100', 
                'rounded-md', 
                'px-3', 
                'py-2', 
                'transition duration-300'
              ]">Add Job
            </RouterLink>
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

.active {
  background-color: #e5e7eb; /* Highlight color */
  font-weight: bold;
}
</style>
