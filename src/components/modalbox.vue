<template>
    <div>
        <div class="modal" tabindex="-1" v-if="abertoBasico === true">
            <div class="modal-dialog">
              <div class="modal-content">
                <div class="modal-header">
                  <h5 class="modal-title">Você se Interessou!</h5>
                  <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                  <p>Voce ja se interessou por este produto e clicou nele { quantidadeBasico } vezes.<br/>Que tal adicioná-lo em seu carrinho de compras?</p>
                </div>
                <div class="modal-footer">
                  <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
                </div>
              </div>
            </div>
          </div>

          <div class="modal" tabindex="-1" v-if="abertoLuxo === true">
            <div class="modal-dialog">
              <div class="modal-content">
                <div class="modal-header">
                  <h5 class="modal-title">Você se Interessou!</h5>
                  <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                  <p>Voce ja se interessou por este produto e clicou nele { quantidadeLuxo } vezes.<br/>Que tal adicioná-lo em seu carrinho de compras?</p>
                </div>
                <div class="modal-footer">
                  <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
                </div>
              </div>
            </div>
          </div>

          <div class="modal" tabindex="-1" v-if="abertoBusiness === true">
            <div class="modal-dialog">
              <div class="modal-content">
                <div class="modal-header">
                  <h5 class="modal-title">Você se Interessou!</h5>
                  <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                  <p>Voce ja se interessou por este produto e clicou nele { quantidadeBusiness } vezes.<br/>Que tal adicioná-lo em seu carrinho de compras?</p>
                </div>
                <div class="modal-footer">
                  <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
                </div>
              </div>
            </div>
          </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent ({
    name: 'ModalBox',

    data(){
        return{
            abertoBasico: false,
            abertoLuxo: false,
            abertoBusiness: false,
            quantidadeBasico: 0,
            quantidadeLuxo: 0,
            quantidadeBusiness: 0
        }
    },

    methods: {
        async cliquesBasico(){
            this.abertoBasico = true
            this.abertoLuxo = false
            this.abertoBusiness = false
            this.quantidadeBasico = this.quantidadeBasico + 1
        },

        async cliquesLuxo(){
            this.abertoBasico = false
            this.abertoLuxo = true
            this.abertoBusiness = false
            this.quantidadeLuxo = this.quantidadeLuxo + 1
        },

        async cliquesBusiness(){
            this.abertoBasico = false
            this.abertoLuxo = false
            this.abertoBusiness = true
            this.quantidadeBusiness = this.quantidadeBusiness + 1
        }
    }
})
</script>