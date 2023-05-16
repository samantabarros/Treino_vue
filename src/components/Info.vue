<template>
  <div>
    <p v-if= esta_trabalhando>Estou trabalhando no momento. </p>
    <p v-else>Estou em busca de novas oportunidades. </p>
    <p>Utilizo as seguintes tecnologias: </p>
    <ul>
      <li>JavaScript</li>
      <li>PHP</li>
      <li>Python</li>
    </ul> 
    <div>
      <button @click="showEmail"> {{textoBotao}} </button>
    </div>
    <p v-show='mostrar_email'>Mande uma mensagem para: {{email}} </p>
    <p>Para acessar meu portfólio<a v-bind:href="meu_link" target="_blank"> basta clicar aqui</a></p>
    <Picture/>
    <Form/>
  </div>
</template>

<script>
import Picture from './form/Picture.vue'
import Form from './Form.vue'

  export default{
    name: 'Info',
    components: { 
      Picture,
      Form 
    },
    data(){
      return{
        esta_trabalhando: false,
        email: 'teste@gmail.com',
        mostrar_email: true,
        meu_link: 'https://www.google.com',
        textoBotao: 'Mostrar email'
      }
    },
    methods: {
      showEmail(){
        this.mostrar_email = !this.mostrar_email
        if(!this.mostrar_email){
          this.textoBotao = 'Mostrar email'
        }else{
          this.textoBotao = 'Esconder email'
        }
      }
    }
  }
</script>
