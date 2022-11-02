<template>
    <div class="rodape__conteudo">
        <p class="rodape__informacao">Projeto Desenvolvido por João Pedro do Carmo R. - 2022 <br/>Utiliza-se VueJS 3 aqui <br/>Responsividade não está disponível neste projeto!</p>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    name: 'RodapeInformativo'
})
</script>

<style scoped>
    .rodape__informacao{
        color: #000000;
        text-align: center;
        font-family: 'Roboto Condensed', sans-serif;
        font-size: 18px;
        margin: 0;
    }
</style>