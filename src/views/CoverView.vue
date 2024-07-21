<template>
  <main class="main-container">
    <div class="row justify-content-center align-items-center" style="height: 460px">
      <div class="col-lg-4 text-center">
        <img
          src="../assets/myphoto/myphoto.jpeg"
          class="bd-placeholder-img rounded-circle m-auto"
          width="140"
          height="140"
          role="img"
          aria-label="Placeholder: 140x140"
          preserveAspectRatio="xMidYMid slice"
          focusable="false"
        />
        <h2>Aji Sampurno</h2>
        <p>Full Stack Web Developer | Bachelor of Information Technology</p>
        <p>
          <router-link to="/about" class="btn btn-secondary"> View details &raquo; </router-link>
        </p>
      </div>
    </div>
  </main>
</template>

<style scoped>
.main-container {
  padding-top: 100px;
  background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
  height: 100vh;
  color: #f8f9fa;
}

.bd-placeholder-img {
  display: block;
  margin-left: auto;
  margin-right: auto;
}

h2,
p {
  color: #f8f9fa;
}
</style>
