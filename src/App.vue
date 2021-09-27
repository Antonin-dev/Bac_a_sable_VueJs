<template>
  <div id="app">
    <Display h1Msg="Je suis le h1"/>
    <Compteur/>
  </div>
</template>

<script>
import Display from "@/components/Display";
import Compteur from "@/components/Compteur";

export default {
  name: 'App',
  components: {
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
