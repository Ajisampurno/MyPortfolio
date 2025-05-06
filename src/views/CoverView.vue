<template>
  <Navbar class="navbar-absolute" />
  <main class="main-container d-flex flex-column justify-content-center align-items-center text-center">
    <div class="overlay"></div>
    <div class="profile-container">
      <img
        src="../assets/myphoto/myphoto.jpeg"
        class="profile-img rounded-circle"
        width="180"
        height="180"
        alt="Aji Sampurno"
      />
      <h2 class="mt-3">Aji Sampurno</h2>
      <p class="description">Full Stack Web Developer | Bachelor of Information Technology</p>
    </div>
  </main>
</template>

<script setup>
import Navbar from '@/components/Navbar.vue';
</script>

<style scoped>
.navbar-absolute {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 3; /* Pastikan navbar berada di atas konten lainnya */
}

.main-container {
  position: relative;
  background: url('../assets/background/bg-cover.png') no-repeat center center fixed;
  background-size: cover;
  min-height: 100vh;
  color: #f8f9fa;
  overflow: hidden;
}

.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(30, 60, 114, 0.7); /* Warna overlay */
  z-index: 1;
}

.profile-container {
  position: relative;
  z-index: 2;
  animation: fadeIn 1.5s ease-in-out;
  max-width: 400px;
}

.profile-img {
  display: block;
  margin: auto;
  width: 180px;
  height: 180px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);
}

h2 {
  font-size: 2rem;
  margin-top: 15px;
}

.description {
  font-size: 1.2rem;
  max-width: 80%;
  margin: 0 auto;
}

.shadow-button {
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);
  transition: transform 0.2s;
}

.shadow-button:hover {
  transform: scale(1.05);
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(-20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
