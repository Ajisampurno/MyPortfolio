<template>
  <div class="container">
    <div class="row featurette">
      <div class="col-md-7">
        <h2 class="featurette-heading">Admin-pade</h2>
        <p class="lead">
          A web page or interface specifically designed for e-commerce administrators
        </p>
        <p>
          <router-link to="/about" class="btn btn-secondary">
            <i class="fab fa-github"></i> Github
          </router-link>
        </p>
        <p>
          <a @click="showAlert" class="btn btn-success"> Demo &raquo;</a>
        </p>
      </div>
      <div class="col-md-5">
        <img
          src="https://drive.google.com/file/d/1r-ditmd9RXEFRf5lJkAVeygONbt1e3VS/view?usp=drive_link"
          class="bd-placeholder-img bd-placeholder-img-lg featurette-image img-fluid mx-auto rounded"
          width="500"
          height="500"
          role="img"
          aria-label="Placeholder: 500x500"
          preserveAspectRatio="xMidYMid slice"
          focusable="false"
        />
      </div>
    </div>

    <hr class="featurette-divider" />

    <div class="row featurette">
      <div class="col-md-7 order-md-2 text-right">
        <h2 class="featurette-heading">Hijja</h2>
        <p class="lead">
          WEB e-commerce single page application (SPA) based on Vue JS and Tailwind CSS to sell
          products from Hijja
        </p>
        <p>
          <router-link to="/about" class="btn btn-secondary">
            <i class="fab fa-github"></i> Github
          </router-link>
        </p>
        <p>
          <a @click="showAlert" class="btn btn-success"> Demo &raquo;</a>
        </p>
      </div>
      <div class="col-md-5 order-md-1">
        <img
          src="https://drive.usercontent.google.com/download?id=1r-ditmd9RXEFRf5lJkAVeygONbt1e3VS&export=view&authuser=0"
          class="bd-placeholder-img bd-placeholder-img-lg featurette-image img-fluid mx-auto rounded"
          width="500"
          height="500"
          role="img"
          aria-label="Placeholder: 500x500"
          preserveAspectRatio="xMidYMid slice"
          focusable="false"
        />
      </div>
    </div>

    <hr class="featurette-divider" />
    <!-- /END THE FEATURETTES -->
  </div>
</template>

<script>
import Swal from 'sweetalert2'

export default {
  name: 'MyComponent',
  methods: {
    showAlert(event) {
      event.preventDefault()

      Swal.fire({
        title: 'Maaf!',
        text: 'Untuk sementara demo tidak tersedia',
        icon: 'info',
        confirmButtonText: 'kembali'
      }).then((result) => {
        if (result.isConfirmed) {
          this.$router.push('/project')
        }
      })
    }
  }
}
</script>

<style scoped>
.bd-placeholder-img {
  border-radius: 15px; /* Adjust the radius as needed */
  font-size: 1.125rem;
  text-anchor: middle;
  -webkit-user-select: none;
  -moz-user-select: none;
  user-select: none;
}
.text-right {
  text-align: right;
}

@media (min-width: 500px) {
  .bd-placeholder-img-lg {
    font-size: 3.5rem;
  }
}
</style>
