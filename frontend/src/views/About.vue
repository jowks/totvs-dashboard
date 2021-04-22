<template>
  <div>
    <div id="container-about">
      <v-container>
        <div id="about">
          <h1>Sobre nós</h1>
          <v-divider />
          <h2>
            TOTVS, a maior empresa de tecnologia do Brasil
          </h2>
          <h3>
            Vamos muito além do ERP com um portfólio completo de sistemas e
            plataformas para gestão de empresas de 12 segmentos de mercado,
            serviços financeiros e soluções de business performance.
            <br />
            Nos últimos cinco anos, investimos R$ 1.7 bilhão em pesquisa e
            desenvolvimento para atender as exigências dos nossos mais de 40 mil
            clientes entre micro, pequenas, médias e grandes - de norte a sul do
            Brasil.
          </h3>
        </div>
      </v-container>
    </div>
    <div id="container-extra">
      <v-container>
        <v-row>
          <v-col
            xl="4"
            lg="4"
            md="4"
            sm="2"
            xs="2"
            v-for="(item, i) in items"
            :key="i"
            class="center"
          >
            <div class="img">
              <v-img :src="item.src" max-width="100" />
            </div>
            <div>
              <strong>{{ item.textPrim }}</strong>
              <br />
              {{ item.textSecon }}
            </div>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </div>
</template>

<script>
export default {
  name: "About",
  components: {},
  data: () => ({
    items: [
      {
        textPrim: "+De 10.000 TOTVERS",
        textSecon: "dedicados ao sucesso dos nossos clientes todos os dias",
        src: "https://www.totvs.com/wp-content/uploads/2020/07/icon-1.png",
      },
      {
        textPrim: "IBOVESPA",
        textSecon:
          "primeira empresa de tecnologia (TI) da América Latina a entrar no Ibovespa",
        src: "https://www.totvs.com/wp-content/uploads/2020/07/icon-2.png",
      },
      {
        textPrim: "50% de market share no brasil",
        textSecon: "e 32% na América Latina",
        src: "https://www.totvs.com/wp-content/uploads/2020/07/icon-3.png",
      },
      {
        textPrim: "+De 40 mil clientes em 12 setores",
        textSecon: "do micro e pequeno negócio até as grandes companhias",
        src: "https://www.totvs.com/wp-content/uploads/2020/07/icon-4.png",
      },
      {
        textPrim: "R$ 1.7 BI em pesquisa e desenvolvimento",
        textSecon: "investidos no últimos 5 anos",
        src: "https://www.totvs.com/wp-content/uploads/2020/07/icon-5.png",
      },
      {
        textPrim: "Presença em mais de 40 países",
        textSecon: "com filiais e centros de desenvolvimento",
        src: "https://www.totvs.com/wp-content/uploads/2020/07/icon-6.png",
      },
    ],
  }),
};
</script>

<style lang="scss" scoped>
#container-about {
  background-image: url("https://portalerp.com/images/2020/08/06/totvs-divulga-resultados-do-2o-trimestre-de-2020jpg.jpeg");
  background-position: center;
  background-repeat: no-repeat;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 50vh;

  #about {
    background: rgba($color: #000000, $alpha: 0.4);
    border-radius: 5px;
    padding: 10px;

    h2 {
      color: orange;
    }
    h3 {
      text-align: justify;
    }
  }
}
#container-extra {
  .center {
    text-align: center;
    padding: 20px 60px;

    .img {
      padding: 10px;
      width: 100%;
      display: flex;
      align-items: center;
      justify-content: center;
    }
  }
}
</style>
