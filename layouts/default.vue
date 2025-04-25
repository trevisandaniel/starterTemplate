<template>
  <div class="flex min-h-screen">
    <Sidebar />
    <main class="flex-1 p-6 bg-gray-100">
      <slot />
    </main>
  </div>
</template>

<script setup>
import Sidebar from '~/components/Sidebar.vue'
</script>
