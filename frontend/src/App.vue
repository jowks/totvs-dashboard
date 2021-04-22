<template>
  <v-app>
    <v-app-bar id="app-bar" fixed color="secondary" app>
      <router-link to="/"
        ><v-img id="img-logo" src="@/assets/totvs-logo.png" />
      </router-link>
      <v-spacer />

      <v-menu open-on-hover top offset-y>
        <template v-slot:activator="{ on, attrs }">
          <v-btn text color="white" v-bind="attrs" v-on="on">
            Categorias
            <v-icon>mdi-chevron-down</v-icon>
          </v-btn>
        </template>

        <v-list>
          <v-list-item v-for="(item, index) in items" :key="index">
            <router-link :to="item.src">
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </router-link>
          </v-list-item>
        </v-list>
      </v-menu>
      <v-divider vertical />
      <v-btn text rounded color="white">
        <router-link to="/about">
          Sobre nós
        </router-link>
      </v-btn>
      <v-divider vertical />
      <v-btn rounded color="orange">
        <router-link to="/contact">
          Contato
        </router-link>
      </v-btn>
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>

    <v-footer color="secondary" padless>
      <v-row justify="center" no-gutters>
        <v-col class="secondary py-2 text-center white" cols="12">
          {{ new Date().getFullYear() }} — <strong> TOTVS </strong>
        </v-col>
      </v-row>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: "App",
  components: {},
  data: () => ({
    items: [
      {
        title: "Sobre nós",
        src: "/about",
      },
      {
        title: "Contato",
        src: "/contact",
      },
    ],
  }),
};
</script>

<style lang="scss" scoped>
#app-bar {
  button {
    margin: 10px;
  }
}
#img-logo {
  max-width: 150px;
}
a {
  text-decoration: none;
  color: white !important;
}
</style>
