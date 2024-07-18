<template>
  <div :class="`${bg} p-6 rounded-lg shadow-md`">
    <slot></slot>
  </div>
</template>

<script setup>
  import { defineProps } from 'vue';

  defineProps({
    bg: {
      type: String,
      default: 'bg-white' // Default background color
    }
  });
</script>

<style scoped>
/* Add any scoped styles here */
</style>
