<template>
  <v-container>
      <h1>placeholder</h1>
  </v-container>
</template>

<script>
export default {
    name: 'ListaApi',
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

<style>

</style>