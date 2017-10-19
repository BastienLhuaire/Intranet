<template>
   <nav>
    <div class="nav">
      <ul>
        <li><a href="#">Accueil</a></li>
        <li><a href="#">Liste des collaborateurs</a></li>
        <li><a href="#">Ajouter un collaborateur</a></li>
      </ul>
    </div>
  </nav>
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
  transition: all 0.3s ease;
  text-decoration: none
}

a:hover{
  color: #56ade1;
  text-decoration: underline;
}

nav{
  background-color: #2b2b30;
  padding: 1% 0;
  position: fixed; /* Set the navbar to fixed position */
  top: 0; /* Position the navbar at the top of the page */
  width: 100%; /* Full width */

  -webkit-box-shadow: 0px -7px 9px 14px rgba(0,0,0,0.71);
  -moz-box-shadow: 0px -7px 9px 14px rgba(0,0,0,0.71);
  box-shadow: 0px -7px 9px 14px rgba(0,0,0,0.71);
}

div.nav{
  margin: 0 10%;
}
</style>
