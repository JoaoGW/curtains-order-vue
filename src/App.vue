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

    <section class="about">
      <SobreNos/>
    </section>
  </main>

  <footer>
    <RodapeInformativo/>
  </footer>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

import CabecalhoFixo from './components/cabecalho.vue'
import CarouselPresentation from './components/carousel.vue'
import CategoriasShow from './components/categorias.vue'
import SobreNos from './components/sobrenos.vue'
import RodapeInformativo from './components/rodape.vue'

export default defineComponent({
  components: {
    CabecalhoFixo, //Importa o componente do cabecalho para a página
    CarouselPresentation, //Importa o componente do carossel de modelos para a página
    CategoriasShow, //Importa o componente do show details dos modelos para a página
    SobreNos, //Importa o componente do sobre nós para a página
    RodapeInformativo //Importa o componente do rodapé para a página
  }
})
</script>

<style scoped>

  main{
    background-color: #FDFDFD;
  }

  .categoria, .about{
    width: 80%;
    margin: 0 auto;
  }

  footer{
    border-top: 1px solid #000;
    padding: 2em 0;
  }
</style>