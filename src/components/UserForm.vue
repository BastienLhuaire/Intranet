<template>
  <div class="UserForm">
    <form name="addUser">
      <p class="radio">
        <label for="genderChoice1">Homme</label>
        <input type="radio" id="genderChoice1" name="gender" value="male" checked="true">
        <label for="genderChoice2">Femme</label>
        <input type="radio" id="genderChoice2" name="gender" value="female">
      </p>

      <p>
        <label for="lastname">Nom :</label>
        <input type="text" name="lastname" placeholder="DOE">
      </p>

      <p>
        <label for="firstname">Prénom :</label>
        <input type="text" name="firstname" placeholder="John">
      </p>

      <p>
        <label for="email">Email :</label>
        <input type="email" name="email" placeholder="John.doe@example.com">
      </p>

      <p>
        <label for="phone">Téléphone :</label>
        <input type="tel" name="phone" placeholder="+33612345678">
      </p>

      <p>
        <label for="city">Ville :</label>
        <input type="text" name="city" placeholder="Paris">
      </p>

      <p>
        <label for="country">Pays :</label>
        <input type="text" name="country" placeholder="France">
      </p>

      <p>        
        <label for="photo">Photo :</label>
        <input type="url" name="photo" placeholder="http://">
      </p>

      <input type="submit" value="Envoyer">
    </form>
  </div>
</template>

<script>

import users from '../data/_users.json';

export default {
  name: 'UserForm',

  data () {
    return {
      msg: 'Welcome to Your Search.js'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.UserForm{
  display: flex;
  align-self: center;
  justify-content: center;
  width: 100%;
}

form{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  align-content: space-between;
  font-size: 1.5em;
}

form p{
  display: flex;
}

input{
  width: 39%;
  margin-left: 5%;
  padding: 1.5% 5%;
  float: right;
  flex : 1;
  min-width: 0;
}


input[type="submit"]{
  width: 80%;
  margin-top: 8%;
  font-size: 1em;
  background-color: #ddd;
  border-radius:10px;
  border: 1px solid #000;
  transition: all 0.3s ease;
  -webkit-box-shadow: 2px 2px 16px 0px rgba(0,0,0,0.75);
  -moz-box-shadow: 2px 2px 16px 0px rgba(0,0,0,0.75);
  box-shadow: 2px 2px 16px 0px rgba(0,0,0,0.75);
}

input[type="submit"], input[type="radio"]{
  float: none;
}

input[type="radio"]{
  width: 5%;
}

.radio{
  width: 100%;
}

input[type="submit"]:hover{
  background-color: #2b2b30;
  color: white;
  cursor: pointer;
}

</style>
