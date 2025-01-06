<template>
  <nav class="navbar navbar-expand-lg bg-light sticky-top">
    <div class="container-fluid">
      <!-- Logo dan Teks -->
      <div class="d-flex align-items-center" >
        <img src="assets/img/logo.png" width="80" alt="Logo" />
        <a class="navbar-brand ms-2" href="#" >SMKN 4 TASIKMALAYA</a>
      </div>

      <!-- Tombol untuk Mobile -->
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>

      <!-- Menu Navigasi -->
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item fs-5">
            <nuxt-link to="/">
              <a class="nav-link active" aria-current="page" href="#"
                >Beranda</a
              >
            </nuxt-link>
          </li>
          <li class="nav-item fs-5">
            <nuxt-link to="/Profil">
              <a class="nav-link active" aria-current="page" href="#">Profil</a>
            </nuxt-link>
          </li>
          <li class="nav-item fs-5">
            <nuxt-link to="/Galeri">
              <a class="nav-link active" aria-current="page" href="#">Galeri</a>
            </nuxt-link>
          </li>
          <li class="nav-item fs-5">
            <nuxt-link to="/eskul">
              <a class="nav-link active" aria-current="page" href="#"
                >Ekstrakurikuler</a
              >
            </nuxt-link>
          </li>
          <li class="nav-item fs-5">
            <nuxt-link to="/biodata">
              <a class="nav-link active" aria-current="page" href="#"
                >Biodata</a
              >
            </nuxt-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>
