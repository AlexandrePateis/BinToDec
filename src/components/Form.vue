<template>
  <div>
    <form @submit="sendForm">
      <div>
        <input type="text" v-model="name">
      </div>
      <div>
        <input type="text" v-model="email">
      </div>
      <div>
        <input type="submit">
      </div>
    </form>
  </div>
</template>

<script>
import Input from "./Input.vue";

export default {
  name: "Form",
  components: {
    Input
  },
  data(){
    return{
      name: '',
      email: ''
    }
  },
  methods:{
    sendForm(e){
      
      const name = this.name
      const email = this.email

      e.preventDefault()
      console.log("Enviado")
      console.log(`Nome: ${name}`)
      console.log(`Email: ${email}`)
    }
  }
};
</script>
