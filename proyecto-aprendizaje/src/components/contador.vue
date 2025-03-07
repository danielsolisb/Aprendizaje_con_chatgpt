<script setup>
import { ref } from "vue";

const nombres = ref(["Daniel", "María", "Carlos", "Ana", "Sofía"]);
const nuevoNombre = ref(""); // Variable para capturar el nuevo nombre

const agregarNombre = () => {
  if (nuevoNombre.value.trim() !== "") { // Verifica que no esté vacío
    nombres.value.push(nuevoNombre.value); // Agrega el nombre a la lista
    nuevoNombre.value = ""; // Limpia el input después de agregar
  }
};
const eliminarNombres = () => {
  nombres.value = [];
}
</script>

<template>
  <div class="contador-container">
    <h1>Lista de Nombres</h1>

    <!-- Input para agregar nombres -->
    <input v-model="nuevoNombre" placeholder="Escribe un nombre" />
    <button @click="agregarNombre">Agregar Nombre</button>
    <button @click="eliminarNombres">Eliminar lista</button>

    <!-- Renderizamos la lista con v-for -->
    <ul>
      <li v-for="(nombre, index) in nombres" :key="index">
        {{ index + 1 }}. {{ nombre }}
      </li>
    </ul>
  </div>
</template>

<style scoped>
/* Estilos de la lista */
ul {
  list-style: none;
  padding: 0;
}

li {
  background: rgba(255, 255, 255, 0.1);
  padding: 8px;
  margin: 5px 0;
  border-radius: 5px;
  text-align: center;
}

/* Estilo del input */
input {
  width: 100%;
  padding: 8px;
  margin-bottom: 10px;
  border: 1px solid #ccc;
  border-radius: 5px;
  font-size: 16px;
  text-align: center;
}

/* Estilo del botón */
button {
  background-color: #008CBA;
  color: white;
  border: none;
  padding: 10px;
  font-size: 16px;
  cursor: pointer;
  border-radius: 5px;
  width: 100%;
  margin-bottom: 10px;
}

button:hover {
  background-color: #005f73;
}
</style>
