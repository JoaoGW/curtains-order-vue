<!--Carousel Feito com Bootstrap 5.2.0 padrão, não foram feitas muitas alterações por aqui a partir da versão padrão-->
<template>
    <div id="carouselExampleCaptions" class="carousel slide" data-bs-ride="false">
        <div class="carousel-indicators">
          <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
          <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="1" aria-label="Slide 2"></button>
          <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="2" aria-label="Slide 3"></button>
        </div>
        <div class="carousel-inner">
          <div class="carousel-item active" id="carousel-cat">
            <img src="../assets/IMGs/pexels-vecislavas-popa-1571467.jpg" class="d-block w-100" id="carousel-photo" alt="Basicos">
            <div class="carousel-caption d-none d-md-block">
              <h5>Basicos</h5>
              <p>Some representative placeholder content for the first slide.</p>
            </div>
          </div>
          <div class="carousel-item" id="carousel-cat">
            <img src="../assets/IMGs/pexels-m&w-studios-90317.jpg" class="d-block w-100" id="carousel-photo" alt="Luxo">
            <div class="carousel-caption d-none d-md-block">
              <h5>Luxo</h5>
              <p>Some representative placeholder content for the second slide.</p>
            </div>
          </div>
          <div class="carousel-item" id="carousel-cat">
            <img src="../assets/IMGs/pexels-monica-silvestre-713149.jpg" class="d-block w-100" id="carousel-photo" alt="Business">
            <div class="carousel-caption d-none d-md-block">
              <h5>Business</h5>
              <p>Some representative placeholder content for the third slide.</p>
            </div>
          </div>
        </div>
        <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide="prev">
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide="next">
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Next</span>
        </button>
      </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent ({
    name: 'CarouselPresentation' //Define o nome do componente para exportação
})
</script>

<style scoped>
    #carousel-cat{
        height: 40vh;
    }

    #carousel-photo{
        object-fit: cover;
        height: 40vh;
    }
</style>