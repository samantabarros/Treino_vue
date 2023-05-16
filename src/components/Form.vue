<template>
  <form action="">
    <div>
      <h2>Meu formulário:</h2>
      <div>
        <InputText />
      </div> 
      <div>
        <InputText />
      </div>
      <div> 
        <Submit />
      </div>
    </div>
  </form>   
</template>

<script>
import InputText from './form/InputText.vue'
import Submit from './form/Submit.vue'

  export default{
    name: 'Form',
    components:{
        InputText,
        Submit
    }
  }
</script>
