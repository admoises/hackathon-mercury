<template>
  <div class="catalogo-de-ajuda">
    <!--     <template>
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
                  <a :href="catalogo.link" style="text-decoration: none">
                    <v-avatar size="60">
                      <img :src="catalogo.imagem" :alt="catalogo.nome" />
                    </v-avatar>
                    <v-sheet height="150">
                      <div class="subtitle-2">{{ catalogo.nome }}</div>
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
    </template> -->

    <div class="box">
      <v-card
        v-for="catalogo of catalogoLista"
        :key="catalogo.id"
        class="mx-auto"
        max-width="250"
      >
        <v-img :src="catalogo.imagem" height="150px"></v-img>

        <v-card-title> {{ catalogo.nome }} </v-card-title>

        <!-- <v-card-subtitle> 1,000 miles of wonder </v-card-subtitle> -->

        <v-card-actions>
          <v-btn
            onclick="window.location.href = 'http://pt.stackoverflow.com'"
            color="orange lighten-2"
            text
          >
            <a
              :href="catalogo.link"
              color="inherit"
              style="text-decoration: none"
              >Ir para o site</a
            >
          </v-btn>

          <v-spacer></v-spacer>

          <v-btn icon @click="show = !show">
            <v-icon>{{ show ? "mdi-chevron-up" : "mdi-chevron-down" }}</v-icon>
          </v-btn>
        </v-card-actions>

        <v-expand-transition>
          <div v-show="show">
            <v-divider></v-divider>

            <v-card-text>
              {{ catalogo.descricao }}
            </v-card-text>
          </div>
        </v-expand-transition>
      </v-card>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      catalogoLista: [],
      drawer: null,
      show: false,
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
.box {
  display: flex;
  flex-wrap: wrap;
}
.mx-auto {
  margin: 0.4em;
}
</style>