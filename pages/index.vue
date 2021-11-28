<template>
<main style="padding-bottom: 15em; padding-top: 11em;">
  
  <div >
    
  </div>
  <div >
    
  </div>
  
  
   <form  class="wrapper">
     <div class="formm">
            <div >
             
            </div>
            <form  class="form" @submit.prevent="send">
              <div>
    <h1 class="textcolor" style="padding-bottom: 0.5em;" >Registre-se</h1>
     </div>
              
               <div class="inputfield">
                 <div>
                  <input class="input" type="text"  placeholder="Email"  v-model="$v.email.$model" :class="{ error: $v.email.$error }">
                  </div>
                   <p v-if="$v.email.$error" >
                  Email invalido.
                  </p>
               </div>  
                <div class="inputfield">
                  <div>
                  <input class="input" type="password" placeholder="Senha"  v-model="$v.password.$model" :class="{ error: $v.password.$error }">
                  </div>
                  <p v-if="$v.password.$error" >
                  Preencha este campo.
                  </p>
               </div> 
               <div >
                <button :disabled="$v.$error">Cadastrar-se <i ></i></button>
              </div>
                 <p ><nuxt-link to="/posts" > {{ resultado }} <span >{{ entrar }}</span> </nuxt-link></p> 
                 
            </form>
            </div>
   </form>
</main>
  
</template>

<script>
import { validationMixin } from "vuelidate";
import { required, minLength, email } from "vuelidate/lib/validators";

export default {

  mixins: [validationMixin],

   data () {
      return{
           email:'',
           password:'',
           url:"",
           logo:"imgs/logo.png",
           vinder:"imgs/vinder.png",
      }
    },

    validations: {
    email: { required, email },
    password: { required, minLength: minLength(1) },
  },

    
  methods: {
    send() {
      this.entrar = "";
      this.resultado = "";
      this.$v.$touch();
      if (this.$v.$invalid) return;
      this.password = "";
      this.email = "";
      this.resultado = "Registro Criado! ";
      this.entrar = "Clique aqui para  acessar os posts";
      this.$v.$reset();
    },
  }
}
</script>

<style>
button{
  border-width: 5px;
border-style: solid;
border-color: rgba(133,26,56,1);
background: rgba(133,26,56,1);
color: white;
}
.formm{
 margin-left: auto;
    margin-right: auto;
    width: 15em
}

.textcolor{
  color:rgb(236, 114, 149);

}
html{
  overflow-x: none;
}

/* ===== Scrollbar CSS ===== */
  /* Firefox */
  * {
    scrollbar-width: auto;
    scrollbar-color: rgb(231, 22, 81) #ffffff;
  }

  /* Chrome, Edge, and Safari */
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






  
.wrapper{
max-width: 800px;
width: 100%;
background: #fff;
margin: 50px auto;
box-shadow: 20px 20px 50px -29px rgb(231, 22, 81);
padding: 30px;
}

.wrapper .title{
font-size: 24px;
font-weight: 700;
margin-bottom: 25px;
color: rgb(231, 22, 81);
text-transform: uppercase;
text-align: center;
}

.wrapper .form{
width: 100%;
}

.wrapper .form .inputfield{
margin-bottom: 15px;
display: flex;
align-items: center;
}

.wrapper .form .inputfield label{
 width: 200px;
 color: #757575;
 margin-right: 10px;
font-size: 14px;
}

.wrapper .form .inputfield .input,
.wrapper .form .inputfield .textarea{
width: 100%;
outline: none;
border: 1px solid #d5dbd9;
font-size: 15px;
padding: 8px 10px;
border-radius: 3px;
transition: all .4s ease;
}

.wrapper .form .inputfield .textarea{
width: 100%;
height: 125px;
resize: none;
}

.wrapper .form .inputfield .custom_select{
position: relative;
width: 100%;
height: 37px;
}

.wrapper .form .inputfield .custom_select:before{
content: "";
position: absolute;
top: 12px;
right: 10px;
border: 8px solid;
border-color: #d5dbd9 transparent transparent transparent;
pointer-events: none;
}

.wrapper .form .inputfield .custom_select select{
-webkit-appearance:none;
-moz-appearance:none;
appearance:none;
outline: none;
width: 100%;
height: 100%;
border: 0px;
padding: 8px 10px;
font-size: 15px;
border: 1px solid #d5dbd9;
border-radius: 3px;
}


.wrapper .form .inputfield .input:focus,
.wrapper .form .inputfield .textarea:focus,
.wrapper .form .inputfield .custom_select select:focus{
border: 1px solid rgb(231, 22, 81);
}

.wrapper .form .inputfield p{
 font-size: 14px;
 color: #757575;
}
.wrapper .form .inputfield .check{
width: 15px;
height: 15px;
position: relative;
display: block;
cursor: pointer;
}
.wrapper .form .inputfield .check input[type="checkbox"]{
position: absolute;
top: 0;
left: 0;
opacity: 0;
}
.wrapper .form .inputfield .check .checkmark{
width: 15px;
height: 15px;
border: 2px solid rgb(146, 16, 53);
display: block;
position: relative;
}
.wrapper .form .inputfield .check .checkmark:before{
content: " ";
position: absolute;
top: 0px;
left: 3px;
width: 5px;
height: 10px;
border: 2px solid;
border-color: transparent transparent #fff #fff;
transform: rotate(-35deg);
display: none;
}
.wrapper .form .inputfield .check input[type="checkbox"]:checked ~ .checkmark{
background: rgb(231, 22, 81);
}

.wrapper .form .inputfield .check input[type="checkbox"]:checked ~ .checkmark:before{
display: block;
}

.wrapper .form .inputfield .btn{
width: 50%;
padding: 8px 10px;
font-size: 15px; 
border: 0px;
margin-left: auto;
margin-right: auto;
background: linear-gradient(90deg, rgba(125,0,69,1) 13%, rgba(122,45,84,1) 92%);
color: #fff;
cursor: pointer;
border-radius: 6px;
outline: none;
font-weight: bold;
}

.wrapper .form .inputfield .btn:hover{
background: #000000;
transition: all .5s ease;
}

.wrapper .form .inputfield:last-child{
margin-bottom: 0;
}

@media (max-width:420px) {
.wrapper .form .inputfield{
  flex-direction: column;
  align-items: flex-start;
}
.wrapper .form .inputfield label{
  margin-bottom: 5px;
}
.wrapper .form .inputfield.terms{
  flex-direction: row;
}
}
</style>




