<template>
    <v-container>
        <v-responsive max-width="460">
          <v-text-field
            dense
            flat
            hide-details
            rounded
            solo-inverted
          ></v-text-field>
        </v-responsive>
        <Card/>
        <Card :pessoas="pessoasLista"/>
    </v-container>
</template>


<script>

export default {
    name: 'Inicio',

    data() {
        return {
            DadosPessoais: []
        }
    },
}
</script>

<style scoped>

</style>


