<template>
  <div class="container">
      <h3 class="mt-4 text-center">CARRERA - ING. SISTEMAS COMPUTACIONALES</h3>

      <!-- Tabla de Cabecera (N° control, Nombre, Grado, Periodo) -->
      <table class="table table-bordered table-dark table-striped mt-3">
          <thead>
              <tr>
                  <th scope="col" class="ncontrol">N° control</th>
                  <th scope="col" class="nombre">Nombre</th>
                  <th scope="col" class="grado">Grado</th>
                  <th scope="col" class="periodo">Periodo</th>
              </tr>
          </thead>
          <tbody>
              <tr v-for="(h, index) in cabecera" :key="index">
                  <td class="ncontrol">{{ h.Ncontrol }}</td>
                  <td class="nombre">{{ h.Nombre }}</td>
                  <td class="grado">{{ h.Grado }}</td>
                  <td class="periodo">{{ h.Periodo }}</td>
              </tr>
          </tbody>
      </table>

      <!-- Nueva Tabla (Carrera, Especialidad, Créditos, Plan de estudios) -->
      <table class="table table-bordered table-dark table-striped mt-3">
          <thead>
              <tr>
                  <td scope="col" class="carrera">Carrera</td>
                  <td scope="col" class="especialidad">Especialidad</td>
                  <td scope="col" class="creditos">Créditos</td>
                  <td scope="col" class="plan">Plan de estudios</td>
              </tr>
          </thead>
          <tbody>
            <tr v-for="(h, index) in cabecera" :key="index">
                  <td class="carrera">{{ h.Carrera }}</td>
                  <td class="especialidad">{{ h.Especilidad }}</td>
                  <td class="creditos">{{ h.Creditos }}</td>
                  <td class="plan">{{ h.Planestudio }}</td>
              </tr>
              <tr>
                  <td class="carrera">Ingeniería en Sistemas Computacionales</td>
                  <td class="especialidad">Redes y Programación</td>
                  <td class="creditos">180</td>
                  <td class="plan">Plan 2022</td>
              </tr>
          </tbody>
      </table>

      <!-- Tabla Horario -->
      <table class="table table-dark table-hover mt-4">
          <thead>
              <tr>
                  <th scope="col">Materia</th>
                  <th scope="col">Lunes</th>
                  <th scope="col">Martes</th>
                  <th scope="col">Miércoles</th>
                  <th scope="col">Jueves</th>
                  <th scope="col">Viernes</th>
              </tr>
          </thead>
          <tbody>
              <tr v-for="(h, index) in horario" :key="index">
                  <td>{{ h.materia }}</td>
                  <td>{{ h.lunes }}</td>
                  <td>{{ h.martes }}</td>
                  <td>{{ h.miercoles }}</td>
                  <td>{{ h.jueves }}</td>
                  <td>{{ h.viernes }}</td>
              </tr>
          </tbody>
      </table>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const cabecera = ref([
  { Ncontrol: '22620118', Nombre: 'Kevin Andrew Osorio Aparicio', Grado: '6', Periodo: 'ENE-JUN 25' }
]);

const horario = ref([
  { materia: 'SCD1015 / 685 / LENGUAJES Y AUTÓMATAS I Solano Hernández Miguel Ángel', lunes: '11:00-13:00', martes: '-', miercoles: '11:00-13:00', jueves: '-', viernes: '12:00-13:00' },
  { materia: 'SCD12101 / 685 / REDES DE COMPUTADORAS Sánchez Vázquez Lucía', lunes: '-', martes: '13:00-15:00', miercoles: '-', jueves: '13:00-15:00', viernes: '16:00-17:00' },
  { materia: 'AEI0815 / 685 / PROGRAMACIÓN WEB Israel Martinez', lunes: '-', martes: '17:00-19:00', miercoles: '-', jueves: '17:00-19:00', viernes: '13:00-14:00' },
  { materia: 'SCA1026 / 685 / TALLER DE SISTEMAS OPERATIVOS Cruz Pérez Jorge', lunes: '13:00-15:00', martes: '-', miercoles: '13:00-15:00', jueves: '-', viernes: '-' },
  { materia: 'SCD1001 / 685 / ADMINISTRACIÓN DE BASES DE DATOS García Hernández Hilario Vidal', lunes: '-', martes: '15:00-17:00', miercoles: '15:00-17:00', jueves: '-', viernes: '14:00-15:00' },
  { materia: 'SCD1014 / 685 / LENGUAJES DE INTERFAZ Sánchez Vázquez Lucía', lunes: '-', martes: '15:00-17:00', miercoles: '15:00-17:00', jueves: '-', viernes: '-' },
  { materia: 'SCD1011 / 685 / INGENIERÍA DE SOFTWARE Román Cruz José Alfredo', lunes: '15:00-17:00', martes: '-', miercoles: '-', jueves: '15:00-17:00', viernes: '15:00-16:00' },
]);
</script>

<style scoped>
.container {
  background-color: #1c1c1e;
  padding: 20px;
  border-radius: 12px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.5);
}

table {
  width: 100%;
  border-collapse: collapse;
}

th,
td {
  border: 1px solid #444;
  padding: 10px;
  text-align: center;
}

th {
  background-color: #444;
  font-size: 1.1em;
}

td {
  font-size: 1em;
}

h3 {
  font-family: "Arial", sans-serif;
  color: #f8f9fa;
  text-transform: uppercase;
  text-align: center;
}

.table-bordered th,
.table-bordered td {
  border: 1px solid #444;
}

.table-dark th {
  background-color: #333;
  color: #f8f9fa;
}

.table-dark td {
  background-color: #444;
  color: #f8f9fa;
}

.table-hover tbody tr:hover {
  background-color: #2a2a2a;
}

.ncontrol {
  background-color: #444;
  color: #f8f9fa;
  font-size: 1.1em;
  text-align: center;
}

.nombre {
  background-color: #444;
  color: #f8f9fa;
  font-size: 1.1em;
  text-align: center;
}

.grado {
  background-color: #444;
  color: #f8f9fa;
  font-size: 1.1em;
  text-align: center;
}

.periodo {
  background-color: #444;
  color: #f8f9fa;
  font-size: 1.1em;
  text-align: center;
}

.carrera {
  background-color: #0c0404;
  color: #f8f9fa;
  font-size: 1.1em;
  text-align: center;
}

.especialidad {
  background-color: #000000;
  color: #f8f9fa;
  font-size: 1.1em;
  text-align: center;
}

.creditos {
  background-color: #0c0808;
  color: #f8f9fa;
  font-size: 1.1em;
  text-align: center;
}

.plan {
  background-color: #000000;
  color: #f8f9fa;
  font-size: 1.1em;
  text-align: center;
}
</style>
