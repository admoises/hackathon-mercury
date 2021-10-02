<template>
    <v-container>
        <v-img class="inicio-imagem mb-4"
            max-height="300"
            max-width="400"
            src="https://www.cecierj.edu.br/wp-content/uploads/2021/09/SETEMBRO-1280x640.jpeg"
            alt="Banner Setembro Amarelo"
        ></v-img>
        <h2>Sobre o tema:</h2>
        <v-divider></v-divider>
        <v-container>
            <v-expansion-panels>
                <v-expansion-panel v-for="conteudo of listaConteudos" :key="conteudo.id">
                    <v-expansion-panel-header>{{ conteudo.nome }}</v-expansion-panel-header>
                        <v-expansion-panel-content id="card">
                            <v-img max-width="50px" :src="conteudo.url"></v-img><p> {{ conteudo.texto }}</p>
                        </v-expansion-panel-content>
                    </v-expansion-panel>
            </v-expansion-panels>
                </v-container>
            </v-container>
</template>

<script>
export default {
  name: 'Prevencao',
  data() {
    return {
      listaConteudos: [
        {
          id: 1,
          nome: 'Por quê',
          texto: 'sadhasodhoashfiopashffhposajf',
          url: 'https://www.petz.com.br/blog/wp-content/uploads/2020/04/meu-primeiro-gato.jpg'
        },
        {
          id: 2,
          nome: 'Brasil',
          texto: '',
          url: 'https://www.petz.com.br/blog/wp-content/uploads/2020/04/meu-primeiro-gato.jpg'
        },
        {
          id: 3,
          nome: 'Mundo',
          texto: '',
          url: 'https://www.petz.com.br/blog/wp-content/uploads/2020/04/meu-primeiro-gato.jpg'
        },
        {
          id: 4,
          nome: 'Mais do que uma campanha',
          texto: '',
          url: ''
        }
      ]
    }
  }
  /*
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
  }*/
}
</script>

<style scoped>
  #card .v-img{
    max-width: 50px;
  }
  #card{
    display: flex;
    flex-direction: row;
    justify-content:space-between;
  }
  .inicio-imagem {
    border: solid 2px;
    border-radius: 4px;
  }
</style>