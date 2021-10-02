<template>
  <v-container id="principal">
        <v-btn id="ajuda">
              <a href="https://www.cvv.org.br">Preciso de ajuda urgente</a>
        </v-btn>
        <v-btn id="setama">
              <router-link to="/about">Setembro Amarelo o Ano Inteiro</router-link>
        </v-btn>
        <p class="fim">Hackaton Decola edição Mercury</p>
        <a class="fim" href="https://www.iteris.com.br/">Iteris Consultoria e Software</a>
  </v-container>  
</template>

<script>


export default {
  name: 'home',
  components: {
  }
}
</script>

<style scoped>
#principal{
  height: 100vh;
  background-color: rgb(243, 233, 95);
}
#setama{
  margin-top: 3vh;
  margin-bottom: 3vh;
}

#ajuda{
  margin-top: 3vh;
  margin-bottom: 3vh;
}

.fim{
  margin-top: 65vh;
  color: rgb(46, 46, 36);
}

.fim:hover{
  color: orange;
}

</style>
