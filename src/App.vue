<template>
  <div id="app">
    <h1>Bac à sable VueJs</h1>
    <Display h1Msg="Je suis le h1"/>
    <Compteur/>
    <KeyModifier />
    <VModel />
  </div>
</template>

<script>
import Display from "@/components/Display";
import Compteur from "@/components/Compteur";
import KeyModifier from "@/components/KeyModifier";
import VModel from "@/components/VModel";

export default {
  name: 'App',
  components: {
    VModel,
    KeyModifier,
    Compteur,
    Display
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
