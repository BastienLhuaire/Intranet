<template>
  <div class="container">
    <h1 class="borderBottom">Ajouter un collaborateur</h1>
    <UserForm/>
  </div>
</template>

<script>

import users from '../data/_users.json';
import UserForm from './UserForm';

export default {
  name: 'AddUser',

  data () {
    return {
      users : users
    }
  },
  components : { UserForm }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
