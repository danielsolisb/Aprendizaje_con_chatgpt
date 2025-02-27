<script setup>
import { ref } from "vue";

const contador = ref(0);

const incrementar = () => {
  contador.value++;
};

const reiniciar = () => {
  contador.value = 0;
};
</script>

<template>
  <div class="contenedor-principal">
    <div class="contador-container">
      <h1>Mi contador comienza a jugar</h1>
      <h2>Subele el volumen!!  {{ contador }}</h2>
      <div class="botones">
        <button @click="incrementar">Incrementar</button>
        <button @click="reiniciar">Reiniciar</button>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* Fuente y estilo del contador */
.contador-container {
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(10px);
  color: white;
  padding: 25px;
  border-radius: 15px;
  width: 350px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.4);
  text-align: center;
  font-family: 'Poppins', sans-serif;
}

/* Títulos */
h1 {
  font-size: 24px;
  font-weight: 600;
  margin-bottom: 10px;
}

h2 {
  font-size: 18px;
  font-weight: 500;
  margin-bottom: 15px;
}

/* Botones con mejor tipografía */
/* Botones */
.botones {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

  
button {
    font-family: 'Poppins', sans-serif;
  background: linear-gradient(to right, #008CBA, #005f73);
  color: white;
  border: none;
  padding: 12px;
  font-size: 16px;
  cursor: pointer;
  border-radius: 8px;
  transition: transform 0.2s, opacity 0.3s;
  width: 100%;
}
</style>


