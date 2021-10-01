<template>
<div id="vModel">
  <form>
    <label for="surname">Votre prénom : </label>
    <input type="text" name="surname" id="surname" v-model="surname">
    <label for="name">Votre nom : </label>
    <input type="text" name="name" id="name" v-model="name">
  </form>
  <p>Valeur des input : {{surname}} {{name}}</p>
</div>
</template>

<script>
export default {
  name: "VModel",
  data() {
    return (
        {
          name: "",
          surname: ""
        }
    )
}
}
</script>

<style scoped>
#vModel{
  background-color: lightsalmon;
}
</style>
