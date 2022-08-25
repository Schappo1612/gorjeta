<script setup>
import { ref } from "vue";

const valor2 = ref("");
const valor1 = ref("");
</script>
<template>
  <div class="inputs">
    <input type="number" v-model="valor1" placeholder="Valor da conta" />

    <select name="Qualidade de serviço" id="asd" v-model="gorgeta">
      <option value="5">5% (péssimo)</option>
      <option value="10">10% (ruim)</option>
      <option value="15">15% (OK)</option>
      <option value="20">20% (bom)</option>
      <option value="25">25% (mais que bom)</option>
      <option value="30">30% (ecelente)</option>
    </select>
    <input type="number" placeholder="Quantidade de pessoas" v-model="valor2" />

    <p>Valor por pessoa : R$ {{ (valor1 * (1 + gorgeta / 100)) / valor2 }}</p>
  </div>
</template>

<style>
.inputs {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 10px;
  background-color: white;
}

input {
  margin: 10px;
}

p {
  border: 1px solid black;
  padding: 2px;
  background-color: white;
}
</style>
