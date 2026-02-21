<template>
    <nav class="navbar navbar-expand-lg bg-body-tertiary" data-bs-theme="dark" >
  <div class="container-fluid">
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarTogglerDemo03" aria-controls="navbarTogglerDemo03" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <a class="navbar-brand" href="#">Pizzería de la NONA</a>
    <div class="collapse navbar-collapse" id="navbarTogglerDemo03">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#">Inicio</a>
        </li>
       <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#">Detalle de compra</a>
        </li>
        <li class="nav-item dropdown">
          <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
            Filtrar Precios
          </a>
          <ul class="dropdown-menu">
            <li><a class="dropdown-item" href="#">Menos de $7.000</a></li>
            <li><a class="dropdown-item" href="#">Entre $7.000 y $9.000</a></li>
            <li><a class="dropdown-item" href="#">Sobre $10.000></a></li>
          </ul>
        </li>
      </ul>
      <form class="d-flex" role="search">
        <input class="form-control me-2" type="search" placeholder="Buscador" aria-label="Search"/>
      </form>
    </div>
  </div>
</nav>
</template>

<script setup>

</script>

<style scoped>

</style>