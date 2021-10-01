<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/>
    <Card />
  </div>
</template>

<script>
import Card from './components/Card.vue'
export default {
  name: 'App',
  components:{
    Card
  },
  data(){
    return{
      pessoasLista: []
    }
  },
  created(){
    fetch('https://randomuser.me/api/?page=1&results=25')
    .then(response => response.json())
    .then(json => {
      this.pessoasLista = json.results
      console.log(this.pessoasLista)
    })
  }
}
</script>
<style scoped>
</style>
