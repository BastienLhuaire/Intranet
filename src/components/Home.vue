<template>
  <div class="container">
    <nav>
      <ul>
        <li><a href="#">Accueil</a></li>
        <li><a href="#">Liste des collaborateurs</a></li>
        <li><a href="#">Ajouter un collaborateur</a></li>
      </ul>
    </nav>
    <div class="borderBottom">
      <h1>Bienvenue dans L'intranet</h1>
      <h3>la plate-forme sociale de l'entreprise</h3>
    </div>
    <div>
      <h2>Avez-vous dit bonjour aujourd'hui à ...</h2>
    </div>
    <div class="flexAlignCenter">
      <div class="guyCard">
        <div>
          <img src="../assets/logo.png">
        </div>
        <div>
          <ul>
            <li><h2>John Doe</h2></li>
            <li><p>John.Doe@example.com</p></li>
            <li><p>+33610293992</p></li>
            <li><p>09/12/1988 (28 ans)</p></li>
            <li><p>Paris, France</p></li>
          </ul>
        </div>
      </div>
      <div class="buttonBonjour">
        <button>Dire bonjour à quelqu'un d'autre !</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home',
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

.guyCard{
  display: flex;
  justify-content: center;
  align-items: center;
  align-self: center;
  border: 2px solid black;
  width: 45%;
}

.guyCard li{
  display: block;
  text-align: left;
  font-size: 1.2em;
}

.flexAlignCenter{
  display: flex;
  align-items: center;
  flex-direction: column;
}
.buttonBonjour{
  width: 45%;
}
.buttonBonjour button{
  width: 100%;
  margin-top: 5%;
  padding: 1.2% 0%; 
  font-size: 1.5em;
  border: 2px solid #000;
  border-radius: 10%;
  background-color: #ddd;
}
.buttonBonjour button:hover{
  background-color: #000;
  color: #fff;
  cursor: pointer;
}

</style>
