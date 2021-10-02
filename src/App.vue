<template>
  <v-app>
    
    <v-main>
      <AppTopBar/>
    </v-main>
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/CatalogoAjuda">CatalogoAjuda</router-link>
      <router-link to="/Prevencao">Prevencao</router-link>
    </div>
    <router-view/>
  </v-app>
</template>

<script>
import AppTopBar from './shared/AppTopBar.vue'

export default {
  data: () => ({
  
    }),
  components: {
    AppTopBar,
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
