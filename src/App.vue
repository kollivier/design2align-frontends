<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link>
      <router-link to="/logout">Logout</router-link>
    </div>
    <router-view />
  </div>
</template>

<script>
import routes from "vue-auto-routing";

export default {
  name: "App",
  computed: {
    routes() {
      return routes;
    }
  }
};
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  #nav {
    text-align: center;
    padding-bottom: 30px;
  }
  a {
    font-weight: bold;
    color: #42b983;
    display: block;
    padding: 5px;
    &.router-link-exact-active {
      color: #2c3e50;
    }
  }
}
</style>
