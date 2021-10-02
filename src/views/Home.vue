<template>
  <v-container id="principal">
    <div class="btn-container">
      <v-btn class="btn-style" color="error"><a href="https://www.cvv.org.br"><span id="btn-text">Preciso de ajuda<br> urgente</span></a></v-btn>
      <v-btn class="btn-style" color="primary"><router-link to="/CatalogoAjuda"><span id="btn-text">Setembro Amarelo<br> o Ano Inteiro</span></router-link></v-btn>
    </div>
    <footer>
      <p class="fim">Hackaton Decola edição Mercury</p>
      <a class="fim" href="https://www.iteris.com.br/">Iteris Consultoria e Software</a>
    </footer>    
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
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  background-color: rgb(243, 233, 95);
}

.fim{
  margin-top: auto;
  color: rgb(46, 46, 36);
}

.fim:hover{
  color: orange;
}
#btn-text {
  text-decoration: none;
  color: white;
}
.btn-style {
  margin-top: 10px;
}
.btn-container{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

</style>
