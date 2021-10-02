<template>
    <v-container id="principal">
      <h1 id="titulo">Sobre a aplicação</h1>
      <p id="texto">O grupo decidiu pelo tema Setembro Amarelo por enxergar a possibilidade de 'linkar' nele os<br>
      outros temas. Racismo é sem dúvidas um dos motivos pelos quais pessoas cometem<br>
      suicídio [1], e a pandemia de COVID-19, que trouxe consigo isolamente social nunca antes<br>
      vivenciado pelas gerações atuais, também tem sido um gatilho [2]. </p>
      <a id="link1" href="https://emais.estadao.com.br/noticias/comportamento,setembro-amarelo-racismo-e-exclusao-social-explicam-alto-indice-de-suicidio-entre-negros-no-pais,70003420170">[1] Racismo e sucídio</a>
      <p></p>
      <a id="link2" href="https://g1.globo.com/ro/rondonia/noticia/2021/09/23/setembro-amarelo-taxa-de-suicidio-aumenta-111percent-no-mes-mais-letais-da-pandemia-em-rondonia.ghtml">[2] Pandemia e suicídio</a>
      <v-img id="img1" src="https://gntech.med.br/pub/media/wysiwyg/Capa_-_BLOG_01.png"></v-img>
      <v-divider></v-divider>
      <p class="fim">Hackaton Decola edição Mercury</p>
      <a class="fim" href="https://www.iteris.com.br/">Iteris Consultoria e Software</a>
    </v-container>

</template>

<style>
#principal{
  background-color: rgb(243, 233, 95);
}

#titulo{
  color: rgb(46, 46, 36);
}

#texto{
  color: rgb(46, 46, 36);
  margin-top: 5vh;
  height: 30vh;
}

#img1{
  margin-top: 6vh;
  margin-bottom: 3vh;
  border-radius: 5px;
}

#link1{
  color: rgb(46, 46, 36);
}

#link1:hover{
  color: orange;
}

#link2{
  color: rgb(46, 46, 36);
}

#link2:hover{
  color: orange;
}

.fim{
  color: rgb(46, 46, 36);
}
.fim:hover{
  color: orange;
}
</style>
