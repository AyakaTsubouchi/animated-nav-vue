<template>
  <Header />
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Welcome to Your Vue.js App" />
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Header from "./components/header/Header.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    Header,
  },
};
</script>

<style lang="scss">
@import "./scss/_variables.scss";
body {
  margin: 0;
  padding: 0;
  min-height: 110vh;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: $primary-color;
  background-color: $background-color;

  /* margin-top: 60px; */
}
</style>
