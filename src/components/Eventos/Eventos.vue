<template>
    <div class="container">
       <div class="row mt-4">
          <div>
             <h4>Evento clic</h4>
             <button @click="clic" class="btn btn-danger" type="button"> Aplastame </button>
             <button @click="soyButon" class="btn btn-warning mx-2" type="button"> Aplastame 2 </button>
          </div>
          <div>
             <h4>Evento Change</h4>
             <label class="input-group-text" for=""> Ingresa tu nombre papu</label>
             <input class="form-control mt-2" type="text" id="nombre" @change="nombreE">
             <p>El nombre ingresado es: <strong>{{ nombre }}</strong></p>
          </div>
          <div>
             <h3>Evento mouseenter y mouseleave</h3>
             <div class="text-center" style="color:#ffff; width: 300px; height: 200px; background-color: black; text-align: center; padding: 15px; border-radius: 14px;"
                @mouseenter="mostrarMensaje" @mouseleave="ocultarMensaje">
                <p>Pase el mouse</p>
                <p>{{ mensaje }}</p>
             </div>
          </div>
          <div>
             <h4>Otro Nombre</h4>
             <label class="input-group-text" for=""> Ingresa otro nombre</label>
             <input class="form-control mt-2" type="text" id="otroNombre" @change="otroNombreE">
             <p>El otro nombre ingresado es: <strong>{{ otroNombre }}</strong></p>
          </div>
          <div>
             <h3>Otro Evento mouseenter y mouseleave</h3>
             <div class="text-center" style="color:#ffff; width: 300px; height: 200px; background-color: black; text-align: center; padding: 15px; border-radius: 14px;"
                @mouseenter="mostrarOtroMensaje" @mouseleave="ocultarOtroMensaje">
                <p>Pase el mouse</p>
                <p>{{ otroMensaje }}</p>
             </div>
          </div>
       </div>
    </div>
 </template>
 
 <script>
 export default {
    data() {
       return {
          nombre: '',
          otroNombre: '',
          mensaje: '',
          otroMensaje: ''
       }
    },
    methods: {
       clic() {
          alert("Gracias por darle clic")
       },
       soyButon() {
          alert("Soy un botón")
       },
       nombreE(event) {
          this.nombre = event.target.value
       },
       otroNombreE(event) {
          this.otroNombre = event.target.value
       },
       mostrarMensaje() {
          this.mensaje = "El mouse está dentro del rectángulo"
       },
       ocultarMensaje() {
          this.mensaje = "El mouse está fuera del rectángulo"
       },
       mostrarOtroMensaje() {
          this.otroMensaje = "El mouse está dentro del segundo rectángulo"
       },
       ocultarOtroMensaje() {
          this.otroMensaje = "El mouse está fuera del segundo rectángulo"
       }
    }
 }
 </script>