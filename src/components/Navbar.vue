<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container-fluid">
      <h3>
        <router-link to="/" class="navbar-brand">Aji Sampurno</router-link>
      </h3>
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
        <div class="navbar-nav ms-auto">
          <router-link to="/about" class="nav-link" :class="{ active: isRouteActive('/about') }"
            >About</router-link
          >
          <router-link to="/project" class="nav-link" :class="{ active: isRouteActive('/project') }"
            >Project Experience</router-link
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
