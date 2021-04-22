<template>
  <div>
    <v-container id="container-contact">
      <v-row>
        <v-col>
          <h2>
            PREENCHA COM SEUS DADOS ABAIXO E DÊ UM PASSO IMPORTANTE PARA
            <span>MELHORAR A EFICIÊNCIA E OS RESULTADOS DO SEU NEGÓCIO:</span>
          </h2>
        </v-col>
      </v-row>

      <div class="input">
        <v-form ref="form" v-model="valid" lazy-validation>
          <v-row>
            <v-col xl="6" lg="6" md="6" sm="12" xs="12">
              <v-text-field
                :rules="[(v) => !!v || 'Item is required']"
                label="Nome*"
                required
              ></v-text-field>
            </v-col>
            <v-col xl="6" lg="6" md="6" sm="12" xs="12">
              <v-text-field
                :rules="[(v) => !!v || 'Item is required']"
                label="E-mail Corporativo*"
                required
              ></v-text-field>
            </v-col>
          </v-row>

          <v-row>
            <v-col xl="6" lg="6" md="6" sm="12" xs="12">
              <v-text-field
                :rules="[(v) => !!v || 'Item is required']"
                label="Telefone*"
                required
              ></v-text-field>
            </v-col>
            <v-col xl="6" lg="6" md="6" sm="12" xs="12">
              <v-text-field
                :rules="[(v) => !!v || 'Item is required']"
                label="Celular*"
                required
              ></v-text-field>
            </v-col>
          </v-row>

          <v-row>
            <v-col xl="6" lg="6" md="6" sm="12" xs="12">
              <v-select
                :rules="[(v) => !!v || 'Item is required']"
                :items="cargos"
                label="Cargo*"
                solo
                required
              />
            </v-col>
            <v-col xl="6" lg="6" md="6" sm="12" xs="12">
              <v-select
                :items="departamentos"
                :rules="[(v) => !!v || 'Item is required']"
                label="Departamento*"
                solo
                required
              />
            </v-col>
          </v-row>

          <v-row>
            <v-col xl="12" lg="12" md="12" sm="12" xs="12">
              <v-text-field
                :rules="[(v) => !!v || 'Item is required']"
                label="Nome da Empresa*"
                required
              ></v-text-field>
            </v-col>
            <v-col xl="12" lg="12" md="12" sm="12" xs="12">
              <v-select
                :rules="[(v) => !!v || 'Item is required']"
                :items="segmentos"
                label="Segmento*"
                solo
                required
              />
            </v-col>
          </v-row>

          <v-checkbox
            v-model="checkbox"
            label="Aceito a utilização dos dados cedidos nesse formulário para a realização de um contato comercial."
          />

          <v-btn color="orange" @click="validate"> Enviar </v-btn>
        </v-form>
      </div>
    </v-container>
  </div>
</template>

<script>
export default {
  name: "Contact",
  components: {},
  data: () => ({
    fields: [{}, {}],
    cargos: [
      "Diretor/Gestor Executivo",
      "CEO/Presidente",
      "Vice-presidente",
      "Gerente",
      "Coordernador/Supervisor",
      "Analista/Assistente",
      "Estagiario/Estudante",
      "Outros",
    ],
    departamentos: [
      "Administrativo/Financeiro",
      "Comercial/Financeiro",
      "Operações",
      "TI - Tecnologia da Informação",
      "RH",
      "Tributário/Fiscal",
      "Outros",
    ],
    segmentos: [
      "Agro",
      " Contrução",
      " Distribuição",
      " Educacional",
      " Financial Services",
      " Hospitalidade",
      " Juridico",
      " Logistica",
      " Manufatura",
      " Outros Segmentos",
      " Prestador de Serviços",
      " Saúde",
      " Varejo",
    ],
    checkbox: false,
    valid: true,
  }),
  methods: {
    validate() {
      this.$refs.form.validate();
    },
  },
};
</script>

<style lang="scss" scoped>
#container-contact {
  max-width: 1000px;
  text-align: center;

  // .input {
  //   display: flex;
  //   justify-content: center;
  //   align-items: center;
  // }

  h2 {
    span {
      color: orange;
    }
  }
}
</style>
