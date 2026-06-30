<script setup lang="ts">
import { ref } from 'vue';
import ShoppingCart from './components/ShoppingCart.vue'

const contador = ref(1)
function adicionar() {
  contador.value++
}

function remover() {
  if (contador.value > 1) {
    contador.value--
  }
}
</script>

<template>
  <div>
    <button @click="remover">
      Remove Item
    </button>

    <button @click="adicionar">
      Add Item
    </button>
  </div>
  <ShoppingCart :quantidade="contador" :valor="19.99" />

</template>
