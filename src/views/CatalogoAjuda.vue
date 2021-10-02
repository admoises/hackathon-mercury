<template>
  <div class="catalogo-de-ajuda">
    <template>
      <v-app id="inspire">
        <v-navigation-drawer v-model="drawer" fixed temporary>
        </v-navigation-drawer>
        <v-main class="grey lighten-2">
          <v-container>
            <v-row>
              <template id="1">
                <v-col class="mt-2" cols="12">
                  <strong>Esses conteudos podem te ajudar 🥰</strong>
                </v-col>

                <v-col
                  v-for="catalogo of catalogoLista"
                  :key="catalogo.id"
                  cols="6"
                  md="2"
                >
                  <a :href="catalogo.link">
                    <v-avatar size="60">
                      <img :src="catalogo.imagem" :alt="catalogo.nome" />
                    </v-avatar>
                    <v-sheet height="150">
                      <span>{{ catalogo.nome }}</span>
                    </v-sheet>
                  </a>
                </v-col>
              </template>

              <template id="2" v-for="nn in 4">
                <v-col :key="nn" class="mt-2" cols="12">
                  <strong>Conteudo tipo {{ nn }}</strong>
                </v-col>

                <v-col v-for="j in 6" :key="`${nn}${j}`" cols="6" md="2">
                  <v-sheet height="150"></v-sheet>
                </v-col>
              </template>
            </v-row>
          </v-container>
        </v-main>
      </v-app>
    </template>
  </div>
</template>

<script>
export default {
  data() {
    return {
      catalogoLista: [],
      drawer: null,
    };
  },

  name: "catalogoLista",

  created() {
    fetch("https://it3zxc-default-rtdb.firebaseio.com/setembroamarelo.json")
      .then((resposta) => resposta.json())
      .then((json) => {
        this.catalogoLista = json;
        console.log(this.catalogoLista);
      });
  },
};
</script>

<style scope>
</style>