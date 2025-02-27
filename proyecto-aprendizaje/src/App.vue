<script setup>
import Contador from "./components/Contador.vue";
</script>

<template>
  <div class="app-container">
    <header>
      <h1>🚀 Mi Aplicación con Vue 3</h1>
    </header>
    <main>
      <Contador />
    </main>
  </div>
</template>

<style scoped>
/* Aplicamos la fuente Poppins */
.app-container {
  background: linear-gradient(to bottom, #1a1a1a, #111);
  color: white;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  font-family: 'Poppins', sans-serif;
}

/* Encabezado */
header {
  width: 100%;
  padding: 20px 0;
  background: rgba(0, 0, 0, 0.3);
  text-align: center;
  font-size: 28px;
  font-weight: 600;
  border-bottom: 2px solid rgba(255, 255, 255, 0.2);
}
</style>
