<template>
  <header>
    <CabecalhoFixo/>
  </header>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import CabecalhoFixo from './components/cabecalho.vue'

export default {
  components: {
    CabecalhoFixo //Importa o componente do cabecalho a página
  }
}
</script>

<style></style>