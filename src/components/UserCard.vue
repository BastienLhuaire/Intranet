<template>
  <div class="guyCard">
    <div>
      <img :src="user.photo">
    </div>
    <div>
      <ul>
        <!-- On remplie les infos avec les valeurs fournis en prop -->
        <li><h2>{{fullname}}</h2></li>
        <li><p>{{user.email}}</p></li>
        <li><p>{{user.phone}}</p></li>
        <li><p>{{user.birthdate}}</p></li>
        <li><p>{{fullLocation}}</p></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'UserCard',
  data () {
    return {
      msg: 'Welcome to Your Search.js'
    }
  },
  props: {
    user : { type: Object, required: true }
  },
  computed : {
    //on concaténe le nom/prénom ainsi que la ville/pays pour écrire plus simplement 
    fullname : function() {
      return this.user.firstname+" "+this.user.lastname;
    },
    fullLocation : function(){
      return this.user.city+", "+this.user.country;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  
.guyCard{
  display: flex;
  justify-content: center;
  align-items: center;
  align-self: center;
  border-top-left-radius: 25px;
  border-bottom-right-radius: 25px;
  width: 45%;
  max-height: 40%;
  margin-bottom: 5.2%;
  background-color: rgba(78,222,255,0.41);

  -webkit-box-shadow: inset 4px 4px 22px 0px rgba(0,0,0,0.75);
  -moz-box-shadow: inset 4px 4px 22px 0px rgba(0,0,0,0.75);
  box-shadow: inset 4px 4px 22px 0px rgba(0,0,0,0.75);
}

.guyCard li{
  display: block;
  text-align: left;
  font-size: 1.2em;
}

img{
  border-radius: 50%;
}
</style>
