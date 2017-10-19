<template>
  <div class="container">
    <nav>
      <ul>
        <li><a href="#">Accueil</a></li>
        <li><a href="#">Liste des collaborateurs</a></li>
        <li><a href="#">Ajouter un collaborateur</a></li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'NavBar',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

nav ul {
  list-style-type: none;
  padding: 0% 2%;
  display: flex;
  justify-content: space-between;
}

li {
  display: inline-block;
  margin: 0 10px;
  font-size: 1.7em;
  font-weight: bold;
}

a {
  color: white;
  font-size: bold;
}

a:hover{
  color: #000;
}

nav{
  background-color: #3838fe;
  padding: 1% 0;
}

</style>
