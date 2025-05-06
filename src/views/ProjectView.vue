<script setup>
import Navbar from '@/components/Navbar.vue'
import Project from '@/components/Project.vue'
</script>

<template>
  <header class="mb-auto">
    <Navbar />
  </header>

  <main style="padding-top: 80px;"> <!-- Sesuaikan padding agar konten tidak tertutup navbar -->
    <Project />
  </main>
</template>

<style scoped>
/* Navbar yang tetap di atas saat di-scroll */
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1000; /* Pastikan navbar tetap di atas konten */
}

/* Sesuaikan padding pada konten agar tidak tertutup oleh navbar */
main {
  padding-top: 80px; /* Sesuaikan dengan tinggi navbar */
}
</style>
