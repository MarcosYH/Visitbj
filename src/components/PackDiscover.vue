<template>
  <div class=" container">
    <span class=" fs-4 spanart">Top Destination</span>
    <h1 class=" fw-bold"> NOS PACKS</h1>
    <div class=" d-flex justify-content-center align-items-center">
    <div class="row ">
      <div class=" rounded-4 artcard" style="width: 26rem;" v-for="element in elements" :key="element.id">
        <div class="card">
          <img :src="element.image" class="card-img-top" alt="Image">
          <div class="card-body">
            <h5 class="card-title">{{ element.titre }}</h5>
            <p class="card-text">{{ element.lieu }}</p>
            <p class="card-text">{{ element.prix }} €</p>
            <p class="card-text">{{ element.etoiles }} étoiles</p>
            <div class=" py-3">
              <button class=" btn btn-orange shadow-sm">Réserver </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  </div>
  
</template>
<script>
import {data} from '../stores/dataHome'
export default {
  computed: {
    elements() {
      return data;
    }
  },
  created() {
    // Appel à une action si nécessaire pour récupérer les données
  }
};
</script>

<style>
.artcard{
  position: relative;
  top: 5rem;
}
.spanart{
  color: #ff880f;
}
</style>
