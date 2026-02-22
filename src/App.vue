<template>
<NavBarComponent/>
<HeaderComponent/>

<PizzaGridComponent :pizzas="pizzas"
  @ver-detalle="verDetalle" />

<PizzaModalComponent v-if="mostrarModal"
  :pizza="pizzaSeleccionada"
  @cerrar="mostrarModal = false"
/>

<FooterComponent/>

</template>

<script setup>
import PizzaGridComponent from './components/PizzaGridComponent.vue';
import pizzaData from '../src/assets/data/pizzas.json'
import { ref } from 'vue'
import NavBarComponent from './components/NavBarComponent.vue';
import HeaderComponent from './components/HeaderComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
const pizzas = ref(pizzaData)

const mostrarModal = ref(false)
const pizzaSeleccionada = ref(null)

const verDetalle = (id)=>{
  pizzaSeleccionada.value = pizzas.value.find(p => p.id === id)
  mostrarModal.value = true
}


</script>

<style>

</style>
