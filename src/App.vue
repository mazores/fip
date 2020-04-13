<template>
  <div id="app">
    <Nav />
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/hiv-101">HIV 101</router-link>
    </div>
    <router-view />
  </div>
</template>

<script>
import Nav from "@/components/Nav.vue";

export default {
  components: { 
    Nav 
  }
}
</script>
<style lang="scss">
#app {
  font-family: 'Nunito', sans-serif;
  -webkit-font-smoothing: antialiased;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color:$blue;
    }
  }
}
</style>
