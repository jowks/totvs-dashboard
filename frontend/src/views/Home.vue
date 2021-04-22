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

    <div id="container-segmentos">
      <v-container>
        <v-row>
          <v-col>
            <div class="header-text">
              <h1 style="color: gray">
                ENTENDEMOS SEU SEGMENTO <br />
                TÃO BEM
                <span style="color: orange">QUANTO VOCÊ</span>
              </h1>
              <p>
                O ERP mais utilizado do Brasil não poderia deixar de vir
                acompanhado por sistemas especializados e desenvolvidos de
                acordo com os processos característicos de cada segmento
              </p>
            </div>
          </v-col>
        </v-row>

        <v-row>
          <v-col
            xl="2"
            lg="2"
            md="2"
            sm="2"
            xs="2"
            v-for="(item, i) in segmentos"
            :key="i"
            class="container-card"
          >
            <div class="card">
              <div class="img">
                <v-img :src="item.img" max-width="40" />
              </div>

              <h4>
                {{ item.title }}
              </h4>

              <v-btn rounded color="#37b6c4"> Saiba Mais </v-btn>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </div>
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
    segmentos: [
      {
        title: "AGRO",
        img: "https://www.totvs.com/wp-content/uploads/2020/07/agro.png",
      },
      {
        title: "LOGISTICA",
        img: "https://www.totvs.com/wp-content/uploads/2020/07/logi.png",
      },
      {
        title: "MANUFATURA",
        img: "https://www.totvs.com/wp-content/uploads/2020/07/Camada_832.png",
      },
      {
        title: "DISTRIBUICAO",
        img:
          "https://www.totvs.com/wp-content/uploads/2019/09/icon-distribuicao.png",
      },
      {
        title: "VAREJO",
        img: "https://www.totvs.com/wp-content/uploads/2020/07/Camada_834.png",
      },
      {
        title: "PRESTADORES DE SERVIÇOS",
        img: "https://www.totvs.com/wp-content/uploads/2020/07/Camada_835.png",
      },
      {
        title: "EDUCACIONAL",
        img:
          "https://www.totvs.com/wp-content/uploads/2019/09/icon-educacao.png",
      },
      {
        title: "HOSPITALIDADE",
        img:
          "https://www.totvs.com/wp-content/uploads/2020/07/hospitalidade.png",
      },
      {
        title: "CONSTRUÇÃO",
        img:
          "https://www.totvs.com/wp-content/uploads/2019/09/icon-construcao-de-projetos.png",
      },
      {
        title: "SAÚDE",
        img: "https://www.totvs.com/wp-content/uploads/2019/09/icon-saude.png",
      },
      {
        title: "JURÍDICO",
        img: "https://www.totvs.com/wp-content/uploads/2020/07/Camada_840.png",
      },
      {
        title: "FINANCIAL SERVICES",
        img:
          "https://www.totvs.com/wp-content/uploads/2019/09/icon-servicos-financeiros.png",
      },
    ],
  }),
};
</script>

<style lang="scss" scoped>
#carousel {
  height: 80vh;
}
#container-segmentos {
  background: rgb(245, 245, 245);

  .header-text {
    text-align: center;

    h1 {
      color: gray;
    }

    p {
      color: gray;
    }
  }

  .container-card {
    display: flex;
    justify-content: center;
    align-items: center;
    .card {
      height: 200px;
      border: 1px solid #ccccccff;
      border-radius: 10px;
      text-align: center;
      align-items: center;
      background: white;
      width: 100%;
      height: 100%;
      margin: 0px auto;
      margin-bottom: 20px;

      .img {
        border: 0px solid #ccccccff;
        border-radius: 50%;
        background: #37b6c4;
        width: 100px;
        height: 100px;
        display: flex;
        align-items: center;
        justify-content: center;
        margin: 10px auto;
      }

      h4 {
        color: gray;
      }
    }
    .card:hover {
      transform: scale(1.1);
      box-shadow: 0px 0px 15px black;
    }
  }
}
</style>
