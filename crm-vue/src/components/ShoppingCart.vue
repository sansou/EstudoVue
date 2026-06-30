<script setup lang="ts">
const props = defineProps<{
  quantidade: number
  valor: number
}>()

</script>

<template>
  <div class="shopping-cart">
    <h2>Carrinho de Compras</h2>
    <p v-if="props.quantidade === 0">Seu carrinho está vazio.</p>
    <p v-else>Você tem {{ props.quantidade }} item(s) no seu carrinho.</p>
    <p>Total: R$ {{ (props.quantidade * props.valor).toFixed(2) }}</p>
    <p v-if="props.quantidade * props.valor > 500 ">Parabéns! Você tem direito a frete grátis!</p>
  </div>
</template>
