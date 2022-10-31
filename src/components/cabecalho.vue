<!--Cabecalho Feito com Bootstrap 5.2.0 padrão, não foram feitas muitas alterações por aqui a partir da versão padrão-->
<template>
    <nav class="navbar navbar-expand-lg bg-light">
        <div class="container-fluid">
            <a class="navbar-brand" href="../../public/index.html">Cortinas Premium</a>
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
              <li class="nav-item">
                <a class="nav-link active" aria-current="page" href="../../public/index.html">Home</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#">Catalogo</a>
              </li>
              <li class="nav-item dropdown">
                <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                  Orçamento
                </a>
                <ul class="dropdown-menu">
                  <li><a class="dropdown-item" href="#">Basic</a></li>
                  <li><a class="dropdown-item" href="#">Regular</a></li>
                  <li><a class="dropdown-item" href="#">Premium</a></li>
                </ul>
              </li>
              <li class="nav-item">
                <a class="nav-link">Sobre</a>
              </li>
            </ul>
            <form class="d-flex" role="search">
              <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
              <button class="btn btn-outline-success" type="submit">Search</button>
            </form>
          </div>
        </div>
      </nav>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: 'CabecalhoFixo' //Nome do Componente para exportação
})
</script>