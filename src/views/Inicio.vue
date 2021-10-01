<template>
    <v-container>
<<<<<<< HEAD
        <v-responsive max-width="460">
          <v-text-field
            dense
            flat
            hide-details
            rounded
            solo-inverted
          ></v-text-field>
        </v-responsive>
=======
        <h2>Inicio</h2>
<<<<<<< HEAD
        <Card/>
>>>>>>> dfe677db41424350b262a7afb6b0012386d977b5
=======
        <Card :pessoas="pessoasLista"/>
>>>>>>> 9a1f09222d82ef1acbf3799bf795ef7404d67c60
    </v-container>
</template>


<script>
<<<<<<< HEAD

export default {
    name: 'Inicio',

    data() {
        return {
            DadosPessoais: []
        }
    },
=======
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
>>>>>>> dfe677db41424350b262a7afb6b0012386d977b5
}
</script>

<style scoped>

</style>


