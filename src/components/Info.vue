<template>
  <div>
    <p v-if="areWork">Atualemnte trabalho</p>
    <p>Tenho experiencia com as seguintes tecnologias:</p>
    <ul>
      <li v-for="(tec, index) in tecnologies" v-bind:key="index">{{tec}}</li>
    </ul>
    <div>
      <input type="text" v-model="name" placeholder="Digite outra tecnologia">
      <button @click="addToList">Clique para adicionar</button>
      <button @click="showEmail">{{ textButton }}</button>
    </div>
    <p v-show="show_email">Meu email: {{ email }}</p>
    <p>Meu site, <a v-bind:href="my_link">Clique aqui</a></p>
  </div>
</template>

<script>
export default {
  name: "Info",
  data() {
    return {
      areWork: true,
      email: "alexandre@cfaz.net",
      show_email: false,
      my_link: "https://google.com",
      textButton: "Mostrar Email",
      tecnologies: ['PHP', 'JavaScript', 'Python', 'CSS'],
      name: ''
    };
  },
  methods: {
    showEmail() {
      this.show_email = !this.show_email;
      if (!this.show_email) {
        this.textButton = "Mostrar Email";
      } else {
        this.textButton = "Ocultar";
      }
    },
    addToList(){
      this.tecnologies.push(this.name)
      this.name = ''
    }
  },
};
</script>

<style scoped>
ul{
  list-style: none;
  margin: 4px;
}
li{
  text-align: left;
  padding: 0;
  margin: 0;
}
</style>