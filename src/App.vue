<template>
<PizzaGridComponent :pizzas="pizzas" />

<PizzaModalComponent v-if="mostrarModal"
  :pizza="pizzaSeleccionada"
  @cerrar="mostrarModal = false"
/>

<PizzaGrid 
  :pizzas="pizzas"
  @ver-detalle="verDetalle"
/>

</template>

<script setup>
import PizzaGridComponent from './components/PizzaGridComponent.vue';
import pizzaData from '../src/assets/data/pizzas.json'
import { ref } from 'vue'
const pizzas = ref(pizzaData)

const mostrarModal = ref(false)
const pizzaSeleccionada = ref(null)

/*const verDetalle = (id)=>{
  pizzaSeleccionada.value = pizzas.value.find(p => p.id === id)
  mostrarModal.value = true
}*/


</script>

<style>

</style>
