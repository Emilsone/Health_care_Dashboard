<template>
  <div id="app">
    <router-view />
  </div>
</template>

<script>
export default {
  name: "app",
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Karla:400,700&display=swap");
* {
  font-family: karla;
}
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /*text-align: center;*/
  color: #2c3e50;
}
</style>
