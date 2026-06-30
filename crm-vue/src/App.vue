<script setup lang="ts">
import { ref } from 'vue'

const contador = ref(0)


function adicionar() {
  contador.value++
}

function remover() {

  if (contador.value > 0) {
    contador.value--
  }

}
</script>

<template>
  <div>
    <h2>Quantidade: {{ contador }}</h2>
    <p v-if="contador == 0"> Contador zerado</p>
    <p v-if="contador > 0"> Contador com itens</p>

  </div>

  <div>
      
    <button @click="remover">
      - 
    </button>
    
    <button @click="adicionar">
      +
    </button>
  </div>

</template>