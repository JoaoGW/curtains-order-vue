<!--Arquivo Principal do Projeto, inclui todos os componentes, etc da página-->
<template>
  <header>
    <CabecalhoFixo/>
  </header>

  <main>
    <CarouselPresentation/>
    <section class="categoria">
      <CategoriasShow/>
    </section>
  </main>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

import CabecalhoFixo from './components/cabecalho.vue'
import CarouselPresentation from './components/carousel.vue'
import CategoriasShow from './components/categorias.vue'

export default {
  components: {
    CabecalhoFixo, //Importa o componente do cabecalho para a página
    CarouselPresentation, //Importa o componente do carossel de modelos para a página
    CategoriasShow //Importa o componente do show details dos modelos para a página
  }
}
</script>

<style scoped>

  main{
    background-color: #FDFDFD;
  }

  .categoria{
    width: 80%;
    margin: 0 auto;
  }
</style>