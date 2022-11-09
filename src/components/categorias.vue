<template>
    <div class="categoria__grupo">
        <div class="categoria__um">
            <img class="categoria__imagem" src="../assets/IMGs/basicos.png" alt="">
            <p class="categoria__text">Modelos Básicos</p>
            <button class="categoria__show" type="button" @click="mostrarBasico()"><a class="linker" href="#mostrando">Mostrar Detalhes</a></button>
        </div>

        <div class="categoria__dois">
            <img class="categoria__imagem" src="../assets/IMGs/luxuosos.png" alt="">
            <p class="categoria__text">Modelos Luxuosos</p>
            <button class="categoria__show" type="button" @click="mostrarLuxo()"><a class="linker" href="#mostrando">Mostrar Detalhes</a></button>
        </div>

        <div class="categoria__tres">
            <img class="categoria__imagem" src="../assets/IMGs/business.png" alt="">
            <p class="categoria__text">Modelos Business</p>
            <button class="categoria__show" type="button" @click="mostrarBusiness()"><a class="linker" href="#mostrando">Mostrar Detalhes</a></button>
        </div>
    </div>

    <div class="categoria__seta">
        <img class="categoria__seta--img animate__animated animate__pulse animate__infinite" src="../assets/icons/arrow-down-icon.svg" alt="">
    </div>

    <!--Para caso o padrão esteja ativo-->
    <div class="categoria__mostrando" v-if="padrao === true">
        <div class="categoria__separador__um">
            <img class="categoria__mostrando--imagem" src="../assets/IMGs/pexels-vecislavas-popa-1571453.jpg" alt="">
        </div>
        <div class="categoria__separador__dois">
            <p class="categoria__mostrando__titulo" ref="modelo">{{ tituloPadrao }}</p>
            <p class="categoria__mostrando__descricao" ref="descricao">{{ descricaoPadrao }}</p>
            <p class="categoria__mostrando__precos" ref="precos">{{ precoPadrao }}</p>
            <button class="categoria__mostrando__direcionar" ref="direcionar">{{ botaoPadrao }}</button>
        </div>
    </div>

    <!--Para caso o básico esteja ativo-->
    <section id="mostrando">
        <div class="categoria__mostrando" v-if="basico === true">
            <div class="categoria__separador__um">
                <img class="categoria__mostrando--imagem" src="../assets/IMGs/pexels-vecislavas-popa-1571467.jpg" alt="">
            </div>
            <div class="categoria__separador__dois">
                <p class="categoria__mostrando__titulo" ref="modelo">{{ tituloBasico }}</p>
                <p class="categoria__mostrando__descricao" ref="descricao">{{ descricaoBasico }}</p>
                <p class="categoria__mostrando__precos" ref="precos">{{ precoBasico }}</p>
                <button class="categoria__mostrando__direcionar" ref="direcionar">{{ botaoTrocado }}</button>
            </div>
        </div>
    </section>

    <!--Para caso o luxo esteja ativo-->
    <div class="categoria__mostrando" v-if="luxo === true">
        <div class="categoria__separador__um">
            <img class="categoria__mostrando--imagem" src="../assets/IMGs/pexels-m&w-studios-90317.jpg" alt="">
        </div>
        <div class="categoria__separador__dois">
            <p class="categoria__mostrando__titulo" ref="modelo">{{ tituloLuxo }}</p>
            <p class="categoria__mostrando__descricao" ref="descricao">{{ descricaoLuxo }}</p>
            <p class="categoria__mostrando__precos" ref="precos">{{ precoLuxo }}</p>
            <button class="categoria__mostrando__direcionar" ref="direcionar">{{ botaoTrocado }}</button>
        </div>
    </div>

    <!--Para caso o business esteja ativo-->
    <div class="categoria__mostrando" v-if="business === true">
        <div class="categoria__separador__um">
            <img class="categoria__mostrando--imagem" src="../assets/IMGs/pexels-monica-silvestre-713149.jpg" alt="">
        </div>
        <div class="categoria__separador__dois">
            <p class="categoria__mostrando__titulo" ref="modelo">{{ tituloBusiness }}</p>
            <p class="categoria__mostrando__descricao" ref="descricao">{{ descricaoBusiness }}</p>
            <p class="categoria__mostrando__precos" ref="precos">{{ precoBusiness }}</p>
            <button class="categoria__mostrando__direcionar" ref="direcionar">{{ botaoTrocado }}</button>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import { ModalBox } from './modalbox.vue'
    
export default defineComponent({
    name: 'CategoriasShow', //Define o nome do componente para exportação

    data() {
        return {
            tituloPadrao: "Selecione um Modelo A Cima",
            tituloBasico: "Cortinas Básicas para o dia a dia",
            tituloLuxo: "Cortinas Finas para quem vive em alto padrão",
            tituloBusiness: "Cortinas feitas para quem possui um negócio",
            descricaoPadrao: "Quando você selecionar um modelo acima você verá um breve resumo contendo informações básicas úteis sobre o produto que te ajudarão a decidir entre a nossa variedade de opções disponíveis para todos os tipos de clientes!",
            descricaoBasico: "Para quem comprou a primeira residência agora e precisa de material de qualidade mas sem gastar muito dinheiro. Aqui temos todos os tipos de tecidos que você venha a necessitar. Clique no botão abaixo e faça já a sua cortina conosco!",
            descricaoLuxo: "Para você que precisa complementar sua belíssima residência com uma cortina de material importado de altíssima qualidade feito à mão fio a fio. Garantia de durabilidade e qualidade exclusivos que você só encontrará aqui!",
            descricaoBusiness: "Se você tem um negócio independentemente da dimensão dele e deseja impressionar os seus clientes até nos mais diversos detalhes. Entendemos como está difícil no momento cuidar de algumas partes da decoração devido a grana curta, mas faremos descontos exclusivos para você crescer junto com a gente",
            precoPadrao: "Os preços estarão disponíveis em R$ Brasil",
            precoBasico: "A partir de R$ 1.499,99",
            precoLuxo: "A partir de R$ 3.999,99",
            precoBusiness: "A partir de R$ 6.999,99",
            botaoPadrao: "Selecione a cima",
            botaoTrocado: "Veja mais Deatalhes",
            padrao: true,
            basico: false,
            luxo: false,
            business: false
        }
    },

    methods: {
        async mostrarBasico(){
            this.padrao = false;
            this.basico = true;
            this.luxo = false;
            this.business = false;
        },

        async mostrarLuxo(){
            this.padrao = false;
            this.basico = false;
            this.luxo = true;
            this.business = false;
        },

        async mostrarBusiness(){
            this.padrao = false;
            this.basico = false;
            this.luxo = false;
            this.business = true;
        }
    },

    components: {
        ModalBox
    }
})
</script>

<style scoped>

    *{
        font-family: 'Roboto Condensed', sans-serif;
    }

    .linker{
        color: #000;
        text-decoration: none;
    }

    .categoria__grupo{
        display: flex;
        flex-direction: row;
        justify-content: space-around;
    }

    .categoria__imagem{
        width: 220px;
        height: 220px;
        margin: 1em 0;
    }

    .categoria__um, .categoria__dois, .categoria__tres{
        text-align: center;
        font-size: 1.4em;
        font-weight: 400;
    }

    .categoria__seta{
        text-align: center;
    }

    .categoria__show{
        background: #EB984E;
        border: 1px solid #030303;
        border-radius: 10px;
        padding: .75rem;
    }

    .categoria__seta--img{
        width: 100px;
        height: 100px;
        margin: 3.5em 0;
    }

    .categoria__mostrando{
        display: grid;
        grid-template-columns: 60% 40%;
        grid-template-rows: 100%;
        height: 60vh;
    }

    .categoria__mostrando--imagem{
        height: 500px;
        width: 800px;
        max-height: 500px;
        max-width: 800px;
        object-fit: cover;
        box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;
    }

    .categoria__separador__um{
        grid-column: 1 / 1;
        grid-row: 1 / 1;
    }

    .categoria__separador__dois{
        grid-column: 2 / 2;
        grid-row: 1 / 1;
    }

    .categoria__mostrando__titulo{
        font-size: 3.2em;
        font-weight: bold;
    }

    .categoria__mostrando__descricao{
        font-size: 1.7em;
    }

    .categoria__mostrando__precos{
        font-size: 1.3em;
        color: #0B6A00;
        text-decoration: underline;
    }

    .categoria__mostrando__direcionar{
        border: none;
        background: #EB984E;
        color: #FDFDFD;
        padding: .8rem;
        font-size: 1.25em;
        border-radius: 10px;
        width: 230px;
        height: 60px;
        color: #030303;
        transition: 1s all;
    }

    .categoria__mostrando__direcionar:hover{
        width: 250px;
        height: 70px;
        text-transform: uppercase;
        box-shadow: rgba(0, 0, 0, 0.25) 0px 54px 55px, rgba(0, 0, 0, 0.12) 0px -12px 30px, rgba(0, 0, 0, 0.12) 0px 4px 6px, rgba(0, 0, 0, 0.17) 0px 12px 13px, rgba(0, 0, 0, 0.09) 0px -3px 5px;
        transition: 1s all;
    }

    @media screen and (min-width: 1281px) and (max-width: 1919px) {
        .categoria__mostrando{
            height: 60vh;
            grid-template-columns: 50% 50%;
        }

        .categoria__mostrando--imagem{
            width: 600px;
            height: 400px;
            max-height: 400px;
            max-width: 600px;
        }

        .categoria__mostrando__titulo{
            font-size: 2.2em;
        }
    
        .categoria__mostrando__descricao{
            font-size: 1.4em;
        }
    
        .categoria__mostrando__precos{
            font-size: 1.1em;
        }
    }
</style>