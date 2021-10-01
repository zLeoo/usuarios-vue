<template>
    <v-container>
        
        <v-responsive max-width="360">
          <v-text-field
            denses
            rounded
            solo-inverted      
          >
          </v-text-field>
        </v-responsive>

        <Card/>

    </v-container>
</template>


<script>
import Card from '../components/Card.vue'

export default {
  components: { Card },
    name: 'Inicio',

    computed: {
        Card
    },

    data() {
        return {
            pessoasLista: [],
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


