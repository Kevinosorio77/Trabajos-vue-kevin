<script>
export default {
    data() {
        return {
            //DATOS DE ALUMNOS
            alumnos:[
                { nc: 12345, nombre: 'Kevin', carrera: 'TICS'},
                { nc: 12346, nombre: 'Matra', carrera: 'ISC'},
                { nc: 12347, nombre: 'Abigail', carrera: 'CTB'},
                { nc: 12348, nombre: 'Juan', carrera: 'LBT'},
                { nc: 12349, nombre: 'Alexis', carrera: 'IDS'},
                { nc: 12350, nombre: 'Evelyn', carrera: 'ISC'},
                { nc: 12351, nombre: 'Vanessa', carrera: 'ISC'},
                { nc: 12352, nombre: 'Nancy', carrera: 'ISC'},
            ]
        }
    }
}
</script>

<template>
<div class="container">
    <h3 class="mt-4">Lista de alumnos de trabajo de Andrew</h3>
    <ul>
        <li v-for="alumno in alumnos" :key="alumno.nc">
            <strong class="curved-text">{{ alumno.nombre }}</strong> -
            <strong class="curved-text">{{ alumno.carrera }}</strong>
        </li>
    </ul>
</div>
</template>

<style>
h3 {
    color: black;
    background-color: rgb(175, 223, 70);
    border-radius: 15px;
    padding: 10px;
    text-align: center;
}

ul {
    list-style-type: none;
    padding: 0;
}

li {
    color: rgba(12, 193, 171, 0.9);
    background-color: black;
    border-radius: 15px;
    padding: 20px;
    margin: 10px;
    text-align: center;
    width: 80%;
    margin-left: auto;
    margin-right: auto;
}

.curved-text {
    display: inline-block;
    font-size: 1.2em;
    text-shadow: 1px 1px 2px rgba(255, 255, 255, 0.6);
    transform: rotate(-5deg);
    letter-spacing: 1px;
}
</style>
