<template>
  <div id="app">
    <Navbar /> 
    <Home />
    <Search />
   <AddUser /> 
  </div>
</template>

<script>
import Navbar from './components/Navbar'
import Home from './components/Home'
import Search from './components/Search'
import AddUser from './components/AddUser'

export default {
  name: 'app',
  components: { Home, Search, Navbar, AddUser }
}
</script>

<style>
body{
  background-color: #4cb0f6;
  margin: 5% 0;
  margin-bottom: 0;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

/* class global pour placer un trait noire sous un élèment */
.borderBottom{
  border-bottom: 3px solid #2b2b30;
  padding-bottom: 4%;
  margin-left: 8%;
  margin-right: 8%;
}

.container{
  margin: 0 20%;
  padding-top: 3%;
  padding-bottom: 5%;
  display: flex;
  justify-content: center;
  flex-direction: column;
  border-left: 1px solid #ddd;
  border-right: 1px solid #ddd;
  background-color: white;
}


</style>
