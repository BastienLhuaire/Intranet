<template>
  <div class="guyCard">
    <div>
      <img :src="user.photo">
    </div>
    <div>
      <ul>
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
  border: 2px solid black;
  width: 45%;
  max-height: 40%;
  margin-bottom: 5.2%;
}

.guyCard li{
  display: block;
  text-align: left;
  font-size: 1.2em;
}
</style>
