<template>
  <div class="maj">
      <h2>Composition API</h2>
      <input type="text" v-model="state.entree" @keyup="enMaj">
      <span>{{state.sortie}}</span>
  </div>    
</template>

<script>
import {reactive} from 'vue';
export default {
    name: 'Majuscules',
    setup() {
        let state = reactive({
            entree: '',
            sortie: ''
        });
        function enMaj() {
            state.sortie = state.entree.toUpperCase();
        }
        return {
            state,
            enMaj
        }
    }

}
</script>

<style>

</style>