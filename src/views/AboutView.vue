<script setup>
import Navbar from '@/components/Navbar.vue'
import tentang from '@/components/tentang.vue'
</script>

<template>
  <header class="mb-auto">
    <Navbar />
  </header>

  <main>
    <div class="container main-container">
      <br />
      <tentang />
    </div>
  </main>
</template>

<style scoped>
/* Navbar Fixed */
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 100; /* Pastikan navbar berada di atas konten */
}

/* Menambahkan ruang di atas konten utama agar tidak tertutup navbar */
.main-container {
  padding-top: 80px; /* Sesuaikan dengan tinggi navbar */
}
</style>
