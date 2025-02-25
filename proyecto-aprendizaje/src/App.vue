<script setup>
import { ref, watch } from "vue";  // Importamos ref() para reactividad
import Saludo from "./components/Saludo.vue"; // Importamos el hijo

const nombreUsuario = ref(""); // Variable reactiva
const apellidoUsuario = ref("Solis");
// Vigilar cambios en el apellido y restaurar "Gómez" si queda vacío
watch(apellidoUsuario, (nuevoValor) => {
  if (nuevoValor === "") {
    setTimeout(() => {
      if (apellidoUsuario.value === "") { // Verificamos nuevamente antes de cambiarlo
        apellidoUsuario.value = "Solis";
      }
    }, 1000); // Esperamos 1 segundo antes de restaurarlo
  }
});

</script>

<template>
  <h1>Mi Aplicación con Vue 3</h1>
  
  <!-- Input para capturar el nombre -->
  <input v-model="nombreUsuario" placeholder="Escribe tu nombre" />
  <input v-model="apellidoUsuario" placeholder="Escribe tu apellido" />

  <!-- Enviar nombreUsuario como prop al hijo -->
  <Saludo :nombre="nombreUsuario" :apellido="apellidoUsuario" />

</template>

<style scoped>
input {
  display: block;
  margin: 10px 0;
  padding: 5px;
  font-size: 16px;
}
</style>
