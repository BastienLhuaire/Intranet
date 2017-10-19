<template>
  <div class="container">
    <div class="borderBottom">
      <h1>Bienvenue dans L'intranet</h1>
      <h3>la plate-forme sociale de l'entreprise</h3>
    </div>
    <div>
      <h2>Avez-vous dit bonjour aujourd'hui à ...</h2>
    </div>
    <div class="flexAlignCenter">
      <UserCard :user='user'></UserCard>
      <div class="buttonBonjour">
        <button @click.prevent="randomUser">Dire bonjour à quelqu'un d'autre !</button>
      </div>
    </div>
  </div>
</template>

<script>
import users from '../data/_users.json';
import UserCard from './UserCard';
export default {

  name: 'Home',

  data () {
    return {
      user : null
    }
  },

  methods: {
    randomUser: function() {
      let propRandom = Math.floor((Math.random() * (users.length-1)));
      this.user = users[propRandom];
    }
  },

  created: function () {
    this.randomUser();
  },

  components : { UserCard }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

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
  padding: 1.2% 0%; 
  font-size: 1.5em;
  border: 2px solid #000;
  border-radius: 10px;
  background-color: #ddd;
}
.buttonBonjour button:hover{
  background-color: #000;
  color: #fff;
  cursor: pointer;
}

</style>
