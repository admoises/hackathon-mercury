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
                    <h2><v-expansion-panel-header>{{ conteudo.nome }}</v-expansion-panel-header></h2>
                        <v-expansion-panel-content id="card">
                           <p>{{ conteudo.texto }}</p>
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
          texto: 'Suicidio é assunto sério é deve ser discutido. Segundo dados recolhidos em 2012 pela Organização Mundial de Saúde (OMS), mais de 800 mil pessoas tiram a própria vida todos os anos, sendo 75% destes indivíduos moradores de países de baixa e média renda.'
        },
        {
          id: 2,
          nome: 'Objetivo',
          texto: 'O principal objetivo da campanha é a conscientização sobre a prevenção do suicídio, buscando alertar a população a respeito da realidade da prática no Brasil e no mundo. A melhor forma de se evitar um suicídio é através de diálogos e discussões que abordem o problema. Suicídio é o ato de tirar a própria vida intencionalmente. Também fazem parte deste comportamento os pensamentos suicidas, planos e tentativas de morte, assim como os transtornos relacionados ao problema. Ações devem ser realizadas a fim de sensibilizar a população e os profissionais da área para os sintomas desse problema e para a saúde mental. Assim, fazendo-os entender que isso também é uma questão de saúde pública. Infelizmente para muitos, o suicídio ainda não é visto como um problema de saúde pública, mas sim uma espécie de fraqueza de conduta ou personalidade.'
        },
        {
          id: 3,
          nome: 'Brasil',
          texto: 'Todos os dias, pelo menos 32 brasileiros tiram suas próprias vidas. Todos esses números poderiam ser evitados ou reduzidos consideravelmente se existissem políticas eficazes de prevenção do suicídio.'
        },
        {
          id: 4,
          nome: 'Mundo',
          texto: 'Segundo dados da OMS (Organização Mundial da Saúde), o suicídio continua sendo uma das principais causas de morte em todo o mundo, conforme relatório “Suicide worldwide in 2019”. Todos os anos, mais pessoas morrem como resultado de suicídio do que HIV, malária ou câncer de mama - ou guerras e homicídios. Em 2019, mais de 700 mil pessoas morreram por suicídio: uma em cada 100 mortes, o que levou a OMS a produzir novas orientações para ajudar os países a melhorarem a prevenção do suicídio e atendimento. Estima-se que no mundo acontece um suicídio a cada 40 segundos.'
        },
        {
          id: 5,
          nome: 'Mais do que uma campanha',
          texto: 'Como vimos, o suicídio não é um problema sazonal, mas sim um problema endêmico. Assim, a campanha "Setembro Amarelo" é um símbolo de um tema que precisa ser amplamente discutido pela sociedade. Dado que o estigma social e a falta de consciência continuam a ser as principais barreiras para a procura de ajuda, é fundamental o debate e a aplicação de políticas direcionadas para o tema.'
        }
      ]
    }
  }
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