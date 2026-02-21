<template>
    
    <div class="modal-backdrop-custom">
    <div class="modal-container bg-white rounded shadow p-4">
   
      <div class="text-end">
        <button 
          class="btn-close"
              @click="cerrarModal"
        ></button>
      </div>
        <PizzaCard 
        :pizza="pizza"
        :esModal="true"
      />
    </div>
  </div>
      
</template>

<script setup>
import { defineProps, defineEmits } from "vue"

import PizzaCardComponent from './PizzaCardComponent.vue'
const props = defineProps({
  pizza: {
    type:Object,
    required: true

  }
  
})
const emit = defineEmits(['cerrar'])
const cerrarModal = () => {
  emit('cerrar')
}

</script>

<style scoped>

</style>