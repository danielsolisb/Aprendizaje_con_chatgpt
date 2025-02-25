<script setup>
defineProps({
  nombre: String, // Recibe el nombre desde el padre
  apellido: String
});
</script>

<template>
  <h2>¡Hola, {{ nombre }}! Bienvenido a Vue 3 🚀</h2>
  <h2> de apellido: {{ apellido }}</h2>
</template>

<style scoped>
h2 {
  color: green;
}
</style>
