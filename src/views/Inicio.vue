<template>
    <v-container class="left">
        <v-responsive max-width="460">
          <v-text-field
            dense
            rounded
            solo-inverted
          ></v-text-field>
        </v-responsive>
        <Card/>
        <Card :pessoas="pessoasLista"/>
    </v-container>
</template>


<script>
import Card from '../components/Card.vue'

export default {
    name: 'Inicio',

    computed: {
        Card
    },

    data() {
        return {
            DadosPessoais: []
        }
    },

    created(){
        fetch('https://randomuser.me/api/?page=1&results=25')
        .then(response => response.json())
        .then(json => {
            this.pessoasLista = json.results
        })
    },
}
</script>

<style scoped>

</style>


