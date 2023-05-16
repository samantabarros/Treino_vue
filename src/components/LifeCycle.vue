
<template>
  <div>
    <h1>Meu nome é {{ nome }}</h1>
    <Info />
  </div>
</template>

<script>
import Info from './Info.vue'

export default {
  name: 'LifeCycle',
  components: {
    Info
  },
  data() {
    return { 
      nome: "Ainda não sei"
    }
  },
    //Hooks
    created(){
      setTimeout(() => {
        this.nome = 'Maria'
      }, 1000);
    },

    mounted(){
      setTimeout(() => {
        this.nome = 'Carol'
      }, 2000);
    }
  }
</script>
