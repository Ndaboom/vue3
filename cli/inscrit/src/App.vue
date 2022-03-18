<template>
  <h1>Liste des inscrits</h1>
  <Inscrits_vue :liste="personnes"></Inscrits_vue>
</template>

<script>
import Inscrits_vue from './components/Inscrits.vue';
export default {
    name: 'App',
    components:{
        Inscrits_vue
    },
    data(){
        return {
             personnes: [
                { prenom: "Jean", nom: "Bréhat", age: 20 },
                { prenom: "Léa", nom: "Prijean", age: 25 },
                { prenom: "Chis", nom: "Martin", age: 38 },
                { prenom: "Pierre", nom: "Petit", age: 18 },
            ],
        }
    }
}
</script>

<style>

</style>