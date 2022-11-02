<template>
    <div class="about__conteudo">
        <img class="about__logo" src="../assets/IMGs/logo.png" alt="Logo da Loja Cortinas Premium">
        <p class="about__nome">Cortinas Premium</p>
        <p class="about__sobrenome">Cortinas para todos as necessidades</p>
        <p class="about__desde">Desde 2022</p>
        <p class="about__informacao">Empresa Fictícia*</p>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent ({
    name: 'SobreNos'
})
</script>

<style scoped>

    *{
        font-family: 'Roboto Condensed', sans-serif;
    }

    .about__conteudo{
        text-align: center;
        margin-bottom: 5rem;
    }

    .about__logo{
        width: 400px;
        height: 400px;
    }

    .about__nome{
        font-weight: bold;
        font-size: 35px;
        text-transform: uppercase;
    }

    .about__sobrenome, .about__desde, .about__informacao{
        font-size: 20px;
    }

    .about__informacao{
        text-decoration: underline;
        margin: 0;
    }
</style>