<template>
    <div class="col-md-6 col-lg-4 col-xl-3 mb-4">
        <div class="card bg-dark h-100 shadow-sm">

            <!-- No logré hacer que no se distorsionara la foto. sélo quedaron de un mismo alto en cada carta -->
            <img py-30 :src="pizza.img" :alt="pizza.name" class="card-img" height="375px" />
            <div class="card-body d-flex flex-column">

                <div class="title">

                    <h5 class="card-title text-capitalize">Pizza</h5>

                    <h5 class="card-title text-capitalize">
                        {{ pizza.name }}
                    </h5>
                </div>
                <hr>

                <p v-if="esModal" class="card-text text-muted">
                    {{ pizza.desc }}
                </p>
                <!-- Ingredientes -->
                <div class="ingredients">

                    <h6 class="ingredients-title">Ingredientes:</h6>
<span v-for="(ingrediente, index) in pizza.ingredients" :key="index" class="ingredients-array">

                        {{ ingrediente }}

                    </span>
                </div>
                <hr>
                <!-- Precio -->
                <div class="price">
                    <span class="card-text fw-bold fs-5 mt-auto">Precio $</span> 
                    <span class="card-text fw-bold fs-5 mt-auto">
                         {{ pizza.price }}
                         </span>
                       
                    
                </div>

                <!-- Botón solo si NO es modal -->
                <button v-if="!esModal" class="btn btn-dark px-70" 
                @click="detalle(pizza.id)">
                    
                    Ver más
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
.title {

    display: flex;
        justify-content: start;
}

.card-title {
    padding-top: 0px;
    padding-left: 10px;
}

.card-body {
  
    padding-left: 0px;
    padding-right: 0px;
    background-color: #fff;
    
}

.card-img{
    padding: 50px 10px;
}
.ingredients-title {
    text-align: center;
}

.ingredients{
  display: block;
}
.ingredients-array{

font-size: x-small;

}
.price{
display: flex;
justify-content: center;
}
</style>