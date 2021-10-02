<template>
    <div>
        <v-app-bar app color="#FFD700">
            <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>
            <v-toolbar-title>Projeto Hackathon</v-toolbar-title>
        </v-app-bar>
        <v-navigation-drawer v-model="drawer" absolute temporary>
        <v-list nav dense>
            <v-list-item-group v-model="group" active-class="green--text text--lighten-2">
        
            <router-link to="/">
                <v-list-item>
                    <v-list-item-icon>
                    <v-icon>mdi-home</v-icon>
                    </v-list-item-icon>
                    <v-list-item-title>Início</v-list-item-title>
                </v-list-item>
            </router-link>

            <router-link to="/about">
                <v-list-item>
                    <v-list-item-icon>
                    <v-icon>mdi-account</v-icon>
                    </v-list-item-icon>
                    <v-list-item-title>Sobre</v-list-item-title>
                </v-list-item>
            </router-link>

            <router-link to="/Prevencao">
                <v-list-item>
                    <v-list-item-icon>
                    <v-icon>mdi-account</v-icon>
                    </v-list-item-icon>
                    <v-list-item-title>Prevenção</v-list-item-title>
                </v-list-item>
            </router-link>

            <router-link to="/CatalogoAjuda">
                <v-list-item>
                    <v-list-item-icon>
                    <v-icon>mdi-account</v-icon>
                    </v-list-item-icon>
                    <v-list-item-title>Catalogo Ajuda</v-list-item-title>
                </v-list-item>
            </router-link>

            </v-list-item-group>
        </v-list>
        </v-navigation-drawer>
    </div>
</template>

<script>
export default {
    data: () => ({
        drawer: false,
        group: null,
    }),
    
}
</script>

<style scoped>

</style>