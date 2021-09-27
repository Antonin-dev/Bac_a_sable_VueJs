<template>
  <div id="Compteur">
    <h1>Compteur : {{ compteur }}</h1>
    <button v-on:click="augmenter">Augmenter</button>
    <button v-on:click="diminuer">Diminuer</button>
    <!--  Écoute du click pour effectuer les diferentes méthodes-->
    <div id="container-canvas">
      <canvas v-on:mousemove="coords"></canvas>
<!--      Ecoute du mouvement de la sourie dans le canvas-->
<!--      Une fois l'evenement produit j'effectue la methode pour executer la mise à jour de la data -->
      <p>{{ x }} / {{ y }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Compteur",
  data() {
    return {
      compteur: 0,
      x: 0,
      y: 0
    }
  },
  methods: {
    augmenter: function () {
      this.compteur++;
    },
    diminuer: function () {
      this.compteur--;
    },
    coords: function (e) {
      this.x = e.offsetX;
      this.y = e.offsetY;
    }
  }
}
</script>

<style scoped>
#Compteur {
  background-color: lightgreen;
}

canvas {
  width: 300px;
  height: 200px;
  border: 1px solid #333;
}

#container-canvas {
  margin-top: 10px;
}
</style>
