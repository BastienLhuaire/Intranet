<template>
  <div class="container">
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
</template>

<script>
export default {
  name: 'Liste',
  data () {
    return {
      msg: 'Welcome to Your Liste.js'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

form{
  display: flex;
  justify-content: center;
}

</style>
