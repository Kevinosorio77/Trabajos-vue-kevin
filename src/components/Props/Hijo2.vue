<script setup>
import { ref } from 'vue'

defineProps({
edad: String,
})


</script>

<template>
  <h6>Soy el componente Hijo 2 me llamo cameru</h6>
  <p>{{ edad }}</p>
</template>

<style scoped>

</style>
