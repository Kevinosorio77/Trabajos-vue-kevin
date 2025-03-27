<template>

    <div class="container">
        <h3 class="mt-4">Horario de clases de sistemas</h3>
        <table class="table table-dark table-hover">
  <thead>
    <tr>
      <th scope="col">Hora</th>
      <th scope="col">Lunes</th>
      <th scope="col">Martes</th>
      <th scope="col">Miercoles</th>
      <th scope="col">Jueves</th>
      <th scope="col">Viernes</th>
    </tr>
  </thead>
  <tbody>
   <tr v-for="(h, index) in horario" :key="index"> 
    <td>{{ h.hora }}</td>
    <td>{{h.lunes }}</td>
    <td>{{h.martes }}</td>
    <td>{{h.miercoles }}</td>
    <td>{{h.jueves }}</td>
    <td>{{h.viernes }}</td>
   </tr>
  </tbody>
</table>
    </div>
    
</template>
<script setup>
import {ref} from 'vue';

const horario = ref([
    {hora:'11:00 - 13:00', lunes: 'Lenguajes y Automatas',martes:'Lenguaje de Interfaz',miercoles:'Lenguajes y Automatas',jueves:'',viernes:'Lenguaje y Automatas'},
    {hora:'13:00 - 15:00', lunes: 'Sistemas operativos',martes:'Redes de computadoras',miercoles:'Sistemas operativo',jueves:'Redes de computadoras',viernes:'web'},
    {hora:'15:00 - 17:00', lunes: 'Software',martes:'Base de datos',miercoles:'Base de datos',jueves:'Software',viernes:'software'},
    {hora:'17:00 - 19:00', lunes: '',martes:'Web',miercoles:'Lenguaje de Interfaz',jueves:'web',viernes:'Redes'},
])
</script>