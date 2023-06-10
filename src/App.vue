<script>
// eslint-disable-next-line no-unused-vars
import { RouterLink, RouterView } from 'vue-router'
import exempleImage from './assets/logo.png';

export default {
  data() {
    return {
      isNavbarOpen: false,
      imagePath: exempleImage,
      activeItem: ''
    };
  },
  methods: {
    toggleNavbar() {
      this.isNavbarOpen = !this.isNavbarOpen;
    },
    setActiveItem(item) {
      this.activeItem = item;
    }
  }
};
</script>

<template>
  <header>

    <nav class="navbar navbar-expand-lg navbar-light fixed-top" style="background-color:white;">
      <div class="container">
        <a class="navbar-brand" href="/">
          <div class="logo mobile-image">
            <img :src="imagePath" alt="Image d'exemple" class="img-fluid">
          </div>
        </a>

        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav"
          aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation" @click="toggleNavbar">
          <span class="navbar-toggler-icon"></span>
        </button>

        <div class="collapse navbar-collapse justify-content-center" :class="{ 'show': isNavbarOpen }" id="navbarNav">
          <ul class="navbar-nav">
            <li class="nav-item mx-5" :class="{ 'active': activeItem === 'discover' }">
              <RouterLink to="/" class="nav-link" aria-current="page" @click="setActiveItem('discover')">Découvrir le
                Bénin</RouterLink>
            </li>
            <li class="nav-item mx-5" :class="{ 'active': activeItem === 'history' }">
              <RouterLink to="/history" class="nav-link" @click="setActiveItem('history')">Nos histoires</RouterLink>
            </li>
          </ul>
          <div class="navbouton">
            <button  class="btn btn-orange2 mx-4">Se connecter</button>
            <button class="btn btn-orange" @click="register">S'inscrire</button>
          </div>

        </div>
      </div>
    </nav>
  </header>
  <RouterView />
</template>

<style>
.navbar-nav .nav-item.active .nav-link {
  color: #333;
  font-weight: bold;
}

.btn-orange {
  background-color: #FF8800;
  border-color: #FF8800;
  color: #fff;
  font-weight: bold;
}
.btn-orange2 {
  background-color: #ffffff;
  border-color: #FF8800;
  color: #FF8800;
  font-weight: bold;
}

.btn-orange:hover,
.btn-orange:focus {
  background-color: darkorange;
  border-color: darkorange;
}

.logo {
  position: relative;
  right: 10rem;

}

@media (max-width: 576px) {
  .mobile-image {
    width: auto;
    height: auto;
    left: 1rem;
  }
}
.navbouton{
    position:relative;
    left: 30%;
  }

</style>