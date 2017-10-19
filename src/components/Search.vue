<template>
  <div class="container">
    <div class="formulairPart">
      <h1 class="borderBottom">Liste des collaborateurs</h1>
      <form name="rechercheForm">
        <input type="text" name="recherche" placeholder="Rechercher ...">
        <p>Filtrer par : </p>
        <select name="filtre" form="rechercheForm">
          <option value="nom">Nom</option>
          <option value="age">Age</option>
          <option value="pays">Pays</option>
        </select>
      </form>
    </div>

    <div class="userList">
      <!-- on créer une carte par user dans le tableau users en utilisant le component UserCard et en lui passant les props du User -->
      <UserCard v-for="(user, index) in users" :key='index' :user='user'></UserCard>
    </div>

  </div>
</template>

<script>

import users from '../data/_users.json';
import UserCard from './UserCard';

export default {
  name: 'Search',

  data () {
    return {
      users : users
    }
  },

  components: {
    UserCard
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

form{
  display: flex;
  justify-content: center;
}

.formulairPart{
  padding-bottom: 5%;
}
.userList{
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}

</style>
