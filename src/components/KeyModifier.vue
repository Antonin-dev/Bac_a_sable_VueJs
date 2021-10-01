<template>
  <div id="keyModifier">
    <form>
      <label for="name">Votre nom : </label>
      <input type="text" name="name" id="name" v-on:keyup="keyUpMethod">
      <!--utilisation du keyModifier pour ecouter le relachement des touches du clavier dans un formulaire-->
    </form>
    <p>{{ letterInput }}</p>
  </div>
</template>

<script>
export default {
  name: "KeyModifier",
  data() {
    return {
      letterInput: ""
    }
  },
  methods: {
    keyUpMethod: function (e) {
      //Mis à jour du state
      this.letterInput += e.key;
    }
  }
}
</script>

<style scoped>
#keyModifier{
  background-color: lightpink;
}
</style>
