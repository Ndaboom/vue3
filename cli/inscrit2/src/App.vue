<template>
  <h1>Liste des inscrits</h1>
  <Users_list></Users_list>
</template>

<script>
import Users_list from './components/Users.vue'
export default {
  name: 'App',
  components: {
    Users_list
  }

}
</script>
<style>
  h1 {
    text-align: center;
    margin-bottom: 4rem;
  }  
</style>