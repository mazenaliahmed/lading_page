<script setup lang="ts">
import { RouterView } from 'vue-router'
import AppHeader from './components/layout/header.vue'
import footer from './components/layout/footer.vue'
</script>

<template>
  <div class="min-h-screen flex flex-col">
    <!-- الهيدر -->
    <AppHeader msg="You did it!" />

    <!-- المحتوى -->
    <main class="flex-1">
      <slot />
      <!-- أو لو تستخدم vue-router -->
       <RouterView /> 
    </main>
   <footer />
    <!-- فوتر (اختياري) -->
    <!-- <AppFooter /> -->
  </div>
</template>
