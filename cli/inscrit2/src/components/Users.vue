<template>
  <table class="table">
    <thead>
      <tr>
        <th>Id</th>
        <th>Nom</th>
        <th>Mail</th>
        <th>Ville</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="(un, index) in donnees" :key="index">
          <td>{{index+1}}</td>
          <td>{{un.name.first}} {{un.name.last}}</td>
          <td>{{un.email}}</td>
          <td>{{un.location.city}}</td>
      </tr>
    </tbody>
  </table>
</template>

<script>
export default {
  name: "Users_list",
  data() {
    return {
      donnees: [],
    };
  },
  created() {
    this.axios
      .get("https://randomuser.me/api/?results=10")
      .then((utilisateurs) => {
        this.donnees = utilisateurs.data.results;
      });
  },
};
</script>

<style>
</style>