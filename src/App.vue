<script setup>
import Navbar from '@/components/Navbar.vue'
import Footer from '@/components/Footer.vue'
</script>

<template>
  <header class="mb-auto">
    <Navbar />
  </header>
  <RouterView />
  <Footer />
</template>
