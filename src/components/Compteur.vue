<template>
  <div id="Compteur">
    <h1>Compteur : {{ compteurA }}</h1>
    <button v-on:click="augmenterA">Augmenter</button>
    <button v-on:click="diminuerA">Diminuer</button>
    <!--  Écoute du click pour effectuer les diferentes méthodes-->
    <button v-on:click="augmenterB">Augmenter B</button>
    <!--    Utilisé pour la fonction compute-->

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
      compteurA: 0,
      compteurB: 0,
      x: 0,
      y: 0
    }
  },
  methods: {
    augmenterA: function () {
      this.compteurA++;
    },
    diminuerA: function () {
      this.compteurA--;
    },
    augmenterB: function () {
      this.compteurB++;
      // console.log(this.memo);
    },
    coords: function (e) {
      this.x = e.offsetX;
      this.y = e.offsetY;
    }
  },
  computed: {
    // Les fonction utilisé dans computed s'execute uniquement si la valeur utilisé à l'interieur de la fonction change.
    memo: function () {
      // console.log("memo se lance")
      return this.compteurB > 10 ? "C'est superieur" : "C'est inferieur";
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
