<template>
    <div class="col-md-6 col-lg-4 col-xl-3 mb-4">
        <div class="card h-100 shadow-sm">
            <img :src="pizza.img" :alt="pizza.name" class="card-img-top" height="375px"/>
            <div class="card-body d-flex flex-column">

                <span class="badge bg-secondary mb-2 align-self-start">
                    Pizza
                </span>
                <h5 class="card-title text-capitalize">
                    {{ pizza.name }}
                </h5>

                <p v-if="esModal" class="card-text text-muted">
                    {{ pizza.desc }}
                </p>
                <!-- Ingredientes -->
                <div class="mb-3">
                    <span v-for="(ingrediente, index) in pizza.ingredients" :key="index"
                        class="badge bg-light text-dark border me-1 mb-1">
                        {{ ingrediente }}
                    </span>
                </div>
                <!-- Precio -->
                <p class="card-text fw-bold fs-5 mt-auto">
                    {{ pizza.price }}
                </p>
                <!-- Botón solo si NO es modal -->
                <button v-if="!esModal" class="btn btn-primary w-100" @click="detalle(pizza.id)">
                    <i class="bi bi-eye me-1"></i>
                    Ver detalle
                </button>
            </div>
        </div>
    </div>

</template>

<script setup>

import { defineProps, defineEmits } from "vue"
const emit = defineEmits(['ver-detalle'])
const detalle = (id) => {
    emit('ver-detalle', id)
}
defineProps({
    pizza: {
        type: Object,
        required: true
    }


})
</script>

<style scoped>


</style>