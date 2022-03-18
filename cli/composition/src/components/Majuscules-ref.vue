<template>
  <div class="maj">
      <h2>Composition API</h2>
      <input type="text" v-model="entree" @keyup="enMaj">
      <span>{{sortie}}</span>
  </div>    
</template>

<script>
import {ref} from 'vue';
export default {
    name: 'majuscules_cpm',
    setup() {
        let entree = ref('');
        let sortie = ref('');
        function enMaj() {
            sortie.value = entree.value.toUpperCase();
        }
        return {
            entree,
            sortie,
            enMaj
        }
    }

}
</script>

<style>

</style>