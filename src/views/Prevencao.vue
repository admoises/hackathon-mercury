<template>
    <v-container>
        <v-img src="https://www.tjdft.jus.br/informacoes/programas-projetos-e-acoes/pro-vida/dicas-de-saude/pilulas-de-saude/setembro-amarelo-mes-da-prevencao-do-suicidio/@@download/image/suici2.jpg" alt="Banner Setembro Amarelo"/>
    </v-container>
</template>

<script>
export default {
  name: 'Prevencao',
  data() {
    return {
      setembroAmarelo: []
    }
  },
  created() {
    fetch('https://it3zxc-default-rtdb.firebaseio.com/setembroamarelo.json')
      .then(response => response.json())
      .then(json => {
        this.setembroAmarelo = json;
        console.log(this.setembroAmarelo);
      })
  }
}
</script>

<style scoped>

</style>