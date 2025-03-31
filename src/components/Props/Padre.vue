<script setup>
import { ref } from 'vue'
import Hijo1 from './Hijo1.vue';
import Hijo2 from './Hijo2.vue';



</script>

<template>
    <div class="container">
        <h1>Soy el componente Padre me llamo pablo</h1>
  <Hijo1 class="mt-4" edad="20"/>
  <Hijo2 class="mt-4" edad="15"/>
    </div>

</template>

<style scoped>

</style>
