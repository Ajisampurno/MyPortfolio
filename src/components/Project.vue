<template>
  <div class="container">
    <div class="row featurette">
      <div class="col-md-7">
        <h2 class="featurette-heading">Admin-pade</h2>
        <p class="lead">
          A web page or interface specifically designed for e-commerce administrators
        </p>
        <p>
          <a
            href="https://github.com/Ajisampurno/admin-page.git"
            target="_blank"
            class="btn btn-dark"
          >
            <i class="fab fa-github"></i> Github
          </a>
        </p>
      </div>
      <div class="col-md-5">
        <img
          src="../assets/project/Admin-page.jpg"
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
          <a
            href="https://github.com/Ajisampurno/e-commerce.git"
            target="_blank"
            class="btn btn-dark"
          >
            <i class="fab fa-github"></i> Github
          </a>
        </p>
      </div>
      <div class="col-md-5 order-md-1">
        <img
          src="../assets/project/Hijja.jpg"
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
      <div class="col-md-7">
        <h2 class="featurette-heading">Eiger SBT</h2>
        <p class="lead">
          An online shop project as a sales medium carried out with the team, for this project I
          contributed as a junior full stack programmer, this website uses Laravel, Bootstrap,
          JQuery, MySQL technology
        </p>
        <p>
          <a
            href="https://github.com/Ajisampurno/eigersbt.git"
            target="_blank"
            class="btn btn-dark"
          >
            <i class="fab fa-github"></i> Github
          </a>
        </p>
      </div>
      <div class="col-md-5">
        <img
          src="../assets/project/eigerSBT.jpg"
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
        <h2 class="featurette-heading">Library Management System</h2>
        <p class="lead">Library management system to manage book inventory and members</p>
        <p>
          <a href="https://github.com/Ajisampurno/library.git" target="_blank" class="btn btn-dark">
            <i class="fab fa-github"></i> Github
          </a>
        </p>
      </div>
      <div class="col-md-5 order-md-1">
        <img
          src="../assets/project/library.jpg"
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
      <div class="col-md-7">
        <h2 class="featurette-heading">POS (Point of Sale)</h2>
        <p class="lead">
          POS (Point of Sale) application to help record sales, manage product stock and display
          reports
        </p>
        <p>
          <a href="https://github.com/Ajisampurno/POS.git" target="_blank" class="btn btn-dark">
            <i class="fab fa-github"></i> Github
          </a>
        </p>
      </div>
      <div class="col-md-5">
        <img
          src="../assets/project/pos.jpg"
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
        <h2 class="featurette-heading">SAW Decision Support System</h2>
        <p class="lead">
          Implementation of Decision Support System with SAW (Simple Additive Weighting) Method for
          Selection of Best Employees of PT Essa Santosa
        </p>
        <p>
          <a
            href="https://github.com/Ajisampurno/SPK_SAW_V8.git"
            target="_blank"
            class="btn btn-dark"
          >
            <i class="fab fa-github"></i> Github
          </a>
        </p>
      </div>
      <div class="col-md-5 order-md-1">
        <img
          src="../assets/project/saw.jpg"
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
