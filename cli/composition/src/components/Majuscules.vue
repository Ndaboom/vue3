<template>
  <div class="maj">
    <h2>Composition API</h2>
    <input type="text" v-model="entree" />
    <span>{{ sortie }}</span>
  </div>
</template>

<script>
import { reactive, computed, toRefs } from "vue";
function enMaj() {
  let state = reactive({
    entree: "",
    sortie: computed(() => {
      return state.entree.toUpperCase();
    }),
  });
  return toRefs(state);
}
export default {
  name: "Majuscules",
  setup() {
    let { entree, sortie } = enMaj();
    return {
      entree,
      sortie
    };
  },
};
</script>

<style>
</style>