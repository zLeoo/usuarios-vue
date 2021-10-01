<template>
    <v-container>
        <h2>Inicio</h2>
        <Card :pessoas="pessoasLista"/>
    </v-container>
</template>

<script>
import Card from '../components/Card.vue'
export default {
    name: 'Inicio',
    components: {
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
        })
    }
}
</script>

<style scoped>

</style>


