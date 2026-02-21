<template>

    <div class="row" >
        
            <PizzaCardComponent v-for="pizza in pizzas" :key="pizza.id" :pizza="pizza" />
    </div>

</template>

<script setup>
import defineProps from "vue"
import PizzaCardComponent from './PizzaCardComponent.vue';

defineProps({
    pizzas:
    {
        type: Array,
        required: true

    }


})


</script>

<style scoped></style>