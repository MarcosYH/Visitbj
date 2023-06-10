<template>
  <div class=" headerdiscover">
      <div class=" container header">
        <div class="row">
          <div class="col-lg-6 descheader">
            <h1 class="txt1 ">Découvrez le Bénin,<br /> <span class="txtcolor "> une perle touristique <br /> africaine.
              </span> </h1>
            <p class="txt2">Plongez au cœur de la culture béninoise: réservez votre séjour dès maintenant!</p>
            <div class=" py-3">
              <button class=" btn btn-orange shadow-sm w-50 ">Réserver dès maintenant </button>
            </div>
           
          </div>
          <div class=" col-lg-6 im1">
            <a href="/">
              <img :src="imgheader" alt="Imaged'exemple" class="img-fluid animated-image">
            </a>
          </div>
        </div>
      </div>
  </div>
</template>
 
<script>
import imgheader from '../assets/imgheader1.png';
import beninheader1 from '../assets/beninheader1.png';
export default {
  data() {
    return {
      imgheader: imgheader,
      beninheader1: beninheader1,
    };
  },

};
</script>
 
<style>
.headerdiscover{
  background: #FFF8F0;
  height: 45rem;
}
.btn-orange {
  background-color: #FF8800;
  border-color: #FF8800;
  color: #fff;
  position: relative;
}

.btn-orange:hover,
.btn-orange:focus {
  background-color: darkorange;
  border-color: darkorange;
}

.animated-image {
  transition: transform 0.3s ease-in-out;
}

.animated-image:hover {
  transform: scale(0.8);
}

.header {
  position: relative;
  top: 8rem;
}

.txt1 {
  font-size: 350%;
  font-weight: bold;
}

.txt2 {
  font-size: 150%;
}

.txtcolor {
  color: #FF8800;
}

.im1 {
  background-image: url('../assets/beninheader1.png');
  background-position: 65%;
  background-repeat: no-repeat;
  background-size: 51%;

}
.descheader{
  position: relative;
  top: 7rem;

}
</style>