<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <div class="container-fluid">
      <router-link to="/" class="navbar-brand">Aji Sampurno</router-link>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNavAltMarkup"
        aria-controls="navbarNavAltMarkup"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
        <div class="navbar-nav">
          <router-link to="/" class="nav-link" :class="{ active: isRouteActive('/') }" exact
            >Home</router-link
          >
          <router-link to="/about" class="nav-link" :class="{ active: isRouteActive('/about') }"
            >About</router-link
          >
          <router-link to="/contact" class="nav-link" :class="{ active: isRouteActive('/contact') }"
            >Contact</router-link
          >
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  methods: {
    isRouteActive(route) {
      return this.$route.path === route
    }
  }
}
</script>

<style scoped>
.active {
  font-weight: bold; /* atau gaya visual lain yang menunjukkan link aktif */
}
</style>
