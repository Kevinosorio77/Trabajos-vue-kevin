<script setup>
import { ref } from 'vue'

const bienvenida = ref("Bienvenidos ala seccion de condicionales")
const nombre = ref("Josue israel")
const apellidos = ref("Vasquez")
//defineProps({
  //msg: String,
//})


</script>

<template>
  <div class="container">
    <h2 class="text-center">{{ bienvenida }}</h2>
<div class="col-md-6"></div>
<h6 class="">{{ nombre }}</h6>
<h6>{{ apellidos }}</h6>
  </div>
  


</template>

<style scoped>

</style>
