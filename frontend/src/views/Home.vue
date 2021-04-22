<template>
  <div class="home">
    <v-carousel
      id="carousel"
      :interval="5000"
      hide-delimiters
      :continuous="true"
      :cycle="true"
    >
      <v-carousel-item v-for="(item, i) in items" :key="i" :src="item.src">
      </v-carousel-item>
    </v-carousel>
  </div>
</template>

<script>
export default {
  name: "Home",
  components: {},
  data: () => ({
    items: [
      {
        src:
          "https://www.techlise.com.br/blog/wp-content/uploads/2020/02/totvs-vantagens-e-desvantagens.jpg",
      },
      {
        src:
          "https://static-wp-eqi15-prd.euqueroinvestir.com/wp-content/uploads/2020/07/predio-totvs-min-1.jpg",
      },
      {
        src:
          "https://portalerp.com/images/2020/08/06/totvs-divulga-resultados-do-2o-trimestre-de-2020jpg.jpeg",
      },
    ],
  }),
};
</script>

<style lang="scss" scoped>
#carousel {
  height: 80vh;
}
</style>
