<script>
import imgdst from '../assets/imgdst.png';
export default {
 data() {
   return {
     imagePath: imgdst,
   };
 },
}
</script>
 
 <template>
   <div class="About">
    <div class=" custom-container">
    <div class="row">
      <div class="col-md-6">
        <img :src="imagePath" alt="Image" class="img-fluid imabout">
      </div>
      <div class="col-md-6">
        <h2 class="txt1about py-5">Les meilleures destinations rassemblées en un seul <br> endroit </h2>
        <p class="txt2about"> Créez votre propre itinéraire en fonction de vos préférences 
          et de <br> votre style de voyage. Explorez les lieux les plus captivants 
          du Bénin <br> en suivant un plan sur mesure, conçu spécialement pour vous.
        </p>
        <div class=" py-3">
              <button class=" btn btn-orange shadow-sm w-50">Réserver dès maintenant </button>
            </div>
      </div>
    </div>
  </div>
   </div>
 </template>
 
 
 <style>
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
 .About{
  background: #FFF8F0;
 }
 .imabout{
  position: relative;
 }
 .txt1about{
  font-size: 300%;
  font-weight:bold;
  position: relative;
  margin-top: 5%;
 }
 .custom-container {
  max-width: 90%; 
  margin-left: auto;
  margin-right: auto;
  
}
.txt2about{
  font-size: 150%;
  margin-top: -3rem;
}
 </style>