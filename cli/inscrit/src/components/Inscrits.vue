<template>
  <table border>
      <tr>
          <th>Prénom</th>
          <th>Nom</th>
          <th>Âge</th>
      </tr>    
      <tr v-for="(personne,index) in liste" :key="index">
          <td>{{personne.prenom}}</td>
          <td>{{personne.nom}}</td>
          <td>{{personne.age}}</td>
      </tr>    
  </table>     
</template>

<script>
export default {
    name: 'Inscrits_vue',
    props: ['liste']
}
</script>

<style>
  th {
      background: lightgrey;
      font-size: 140%;
  }
  td {
      width: 10rem;
      text-align: center;
  }

</style>