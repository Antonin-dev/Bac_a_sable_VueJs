<template>
  <div id="Display">
    <h1>{{ h1Msg }}</h1>
    <!--Récuperation de props -->
    <p>{{ calcul(2, 5) }}</p>
    <p>{{ presentation() }}</p>
    <!--Appel de methode -->
    <a v-bind:href="url">Le site de VueJs</a><br>
    <a :href="react">Le site de ReactJs</a>
    <!--Link de la data avec v:bind le shortcut est : -->
  </div>
</template>

<script>
export default {
  name: "Display",
  props: {
    h1Msg: String
  },
  data() {
    return {
      url: "https://vuejs.org/",
      react: "https://reactnative.dev/"
    }
  },
  methods: {
    calcul: function (a, b) {
      return "Le resultat est " + (a + b);
    },
    presentation: function () {
      return this.h1Msg;
    }
  }
}
</script>

<style scoped>
#Display{
  background-color: lightblue;
}
</style>
