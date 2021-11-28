<template>
<div>
<h1 class="textcolo">
    Confira as ultimas atualiações <br> 
    
    &#8595;
</h1>
<div class="container">

    <div class="foraitem">
        <h3>
         <p class="user"><img src="~/static/images/usericon2.png" alt="">Gabriel</p>
         <p class="descricao">Vida boa!</p>
    <div class="item"><b-button id="colorbnt" @click="modalShow1 = !modalShow1"><img src="~/static/images/Natureza1.jpg" alt=""></b-button>
    <div v-if="mostrarcomentario1 === true">
    <div v-for="texto in comentario1" :key="texto.comentario1" >
        <p class="comenalin">Usuario: {{comentario1.conteudo1}}</p>
    </div>
    </div>
    <form >
        <input class="inputalin" v-model="comentario1.conteudo1" v-if="mostrarcomentario1 === false && comentar1 === true">
        <button class="bntalin" @click.prevent="criarcomentario1" v-if="comentar1 === false">Comentar</button>
        <button class="bntalin2" @click.prevent="send1" v-if="mostrarcomentario1 === false && comentar1 === true">Enviar</button>
       
    </form>
    
    <b-modal title="Gabriel" v-model="modalShow1"><img id="fota3" src="~/static/images/Natureza1.jpg" alt=""></b-modal></div>
        </h3>
    </div>






     <div class="foraitem">
        <h3>
         <p class="user"><img src="~/static/images/usericon2.png" alt="">Ana</p>
         <p class="descricao">Amo a praia!</p>
    <div class="item"><b-button id="colorbnt" @click="modalShow2 = !modalShow2"><img src="~/static/images/Natureza2.jpg" alt=""></b-button>
    <div v-if="mostrarcomentario2 === true">
    <div v-for="texto in comentario2" :key="texto.comentario2" >
        <p class="comenalin">Usuario: {{comentario2.conteudo2}}</p>
    </div>
    </div>
    <form >
        <input class="inputalin" v-model="comentario2.conteudo2" v-if="mostrarcomentario2 === false && comentar2 === true">
        <button class="bntalin" @click.prevent="criarcomentario2" v-if="comentar2 === false">Comentar</button>
        <button class="bntalin2" @click.prevent="send2" v-if="mostrarcomentario2 === false && comentar2 === true">Enviar</button>
       
    </form>
    
   <b-modal title="Gabriel" v-model="modalShow2"><img id="fota2" src="~/static/images/Natureza2.jpg" alt=""></b-modal></div>
        </h3>
    </div>







    <div style="padding-bottom: 15em;" class="foraitem">
        <h3>
         <p class="user"><img src="~/static/images/usericon2.png" alt="">Erick</p>
         <p class="descricao">Bora pesca??</p>
    <div class="item"><b-button id="colorbnt2" @click="modalShow3 = !modalShow3"><img src="~/static/images/Natureza3.jpg" alt=""></b-button>
    <div v-if="mostrarcomentario3 === true">
    <div v-for="texto in comentario3" :key="texto.comentario3" >
        <p class="comenalin">Usuario: {{comentario3.conteudo3}}</p>
    </div>
    </div>
    <form >
        <input class="inputalin" v-model="comentario3.conteudo3" v-if="mostrarcomentario3 === false && comentar3 === true">
        <button class="bntalin" @click.prevent="criarcomentario3" v-if="comentar3 === false">Comentar</button>
        <button class="bntalin2" @click.prevent="send3" v-if="mostrarcomentario3 === false && comentar3 === true">Enviar</button>
       
    </form>
    
    <b-modal title="Gabriel" v-model="modalShow3"><img id="fota1" src="~/static/images/Natureza3.jpg" alt=""></b-modal></div>
        </h3>
    </div>
</div>
</div>  
</template>

<script>
  export default {
    data() {
      return {
        modalShow1: false,
        modalShow2: false,
        modalShow3: false,
        
        comentario1: { 
            conteudo1:'', 
        },
        mostrarcomentario1: false,
        comentar1: false,


        comentario2: { 
            conteudo2:'', 
        },
        mostrarcomentario2: false,
        comentar2: false,


        comentario3: { 
            conteudo3:'', 
        },
        mostrarcomentario3: false,
        comentar3: false,
      }
    },
    methods: {

        send1(){
            this.mostrarcomentario1 = true,
            this.mostrarbotao1 = true
        },


        send2(){
            this.mostrarcomentario2 = true,
            this.mostrarbotao2 = true
        },

         send3(){
            this.mostrarcomentario3 = true,
            this.mostrarbotao3 = true
        },

    
    criarcomentario1(){
        this.comentar1 = true
    },


    criarcomentario2(){
        this.comentar2 = true
    },

    criarcomentario3(){
        this.comentar3 = true
    },



    },


  }
</script>


<style>

.user{
    padding-left: 5px;
    padding-top: 5px;
}
.descricao{
    padding-left: 20px;
}

#colorbtn2:hover{
     border-width: 1px;
    border-style: solid;
    border-radius: 0%;
}
#colorbnt2{
    background: rgba(133,26,56,1);
    border-width: 0.1px;
    border-style: solid;
    border-radius: 0%;
}
#colorbtn1:hover{
     border-width: 1px;
    border-style: solid;
    border-radius: 0%;
}
#colorbnt1{
    background: rgba(133,26,56,1);
    border-width: 0.1px;
    border-style: solid;
    border-radius: 0%;
}
#colorbtn:hover{
     border-width: 1px;
    border-style: solid;
    border-radius: 0%;
}
#colorbnt{
    background: rgba(133,26,56,1);
    border-width: 0.1px;
    border-style: solid;
    border-radius: 0%;
}
body{
    background: linear-gradient(0deg, rgba(255,255,255,1) 11%, rgba(215,215,215,1) 92%);
}
h3 p img{
    max-width:50px;
    max-height:50px;
    width: auto;
    height: auto;
    padding-bottom: 0em ;
    
}
h3{
    border-width: 5px;
    border-style: solid;
    border-color: rgba(133,26,56,1);
    padding-bottom: 0em;
}

.container{
   margin-left: auto;
    margin-right: auto;
    width: 26.5em
}
.container div div img{
    max-width:350px;
    max-height:600px;
    width: auto;
    height: auto;
    padding-bottom: 0em ;
}
#fota1{
    max-width:465px;
    max-height:600px;
    padding-bottom: 0em
}
#fota2{
    max-width:465px;
    max-height:600px;
    padding-bottom: 0em
}
#fota3{
   max-width:465px;
    max-height:600px;
    padding-bottom: 0em
}
.foraitem{
    padding-bottom: 6em;
}
.item{
    border-width: 5px;
    border-style: solid;
    border-color: rgba(133,26,56,1);
    
}

.textcolo{
    padding-top: 2em;
    text-align: center;
    padding-bottom: 3em;
    color: rgba(125,0,69,1) ;
    
}

@media (max-width:420px){
    .container div div img{
    max-width:164px;
    max-height:400px;
    width: auto;
    height: auto;
    padding-bottom: 0em ;
}
.container{
   margin-left: auto;
    margin-right: auto;
    width: 15em
}

}



@media (max-width:230px){
    .container div div img{
    max-width:85px;
    max-height:250px;
    width: auto;
    height: auto;
    padding-bottom: 0em ;
}
.container{
   margin-left: auto;
    margin-right: auto;
    width: 10em
}

}

@media (max-width:520px){
#fota1{
    max-width:450px;
    max-height:600px;
    padding-bottom: 0em
}
#fota2{
    max-width:450px;
    max-height:600px;
    padding-bottom: 0em
}
#fota3{
   max-width:450px;
    max-height:600px;
    padding-bottom: 0em
}

}

@media (max-width:400px){
#fota1{
    max-width:310px;
    max-height:600px;
    padding-bottom: 0em
}
#fota2{
    max-width:310px;
    max-height:600px;
    padding-bottom: 0em
}
#fota3{
   max-width:310px;
    max-height:600px;
    padding-bottom: 0em
}

}











* {
    scrollbar-width: auto;
    scrollbar-color: #1cca76 #ffffff;
    
  }

  
  *::-webkit-scrollbar {
    width: 16px;
  }

  *::-webkit-scrollbar-track {
    background: #ffffff;
  }

  *::-webkit-scrollbar-thumb {
    background: linear-gradient(0deg, rgba(125,0,69,1) 13%, rgba(184,43,73,1) 92%);
    border-radius: 10px;
    border: 3px solid #ffffff;


  }


.bntalin{ 
    width: 150px; 
    margin: 10px -80px; 
    position:relative;
    top:50%; 
    left:50%;
    border-width: 5px;
    border-style: solid;
    border-color: rgba(133,26,56,1);
    background: rgba(133,26,56,1);
    color: white;
}


.bntalin2{ 
    width: 150px; 
    margin: 10px -80px; 
    position: relative;
    display: grid;
    left:50%;
    border-width: 5px;
    border-style: solid;
    border-color: rgba(133,26,56,1);
    background: rgba(133,26,56,1);
    color: white;
}


.inputalin{
    width: 371px; 
    margin: 10px -185px; 
    position:relative;
    top:50%; 
    left:50%;
    
}

@media (max-width:420px){
    .inputalin{
    width: 169px; 
    margin: 10px -185px; 
    position:relative;
    top:50%; 
    left:7em;
    
}

}

.comenalin{
    padding-left: 10px;
    font-size: 20px;
}

</style>