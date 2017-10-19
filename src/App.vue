<template>
  <div id="app">
    <Liste/>
  </div>
</template>

<script>
import Liste from './components/Liste'

export default {
  name: 'app',
  components: {
    Liste
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.borderBottom{
  border-bottom: 3px solid black;
  padding-bottom: 4%;
  margin-left: 8%;
  margin-right: 8%;
}

.container{
  margin: 0 20%;
  display: flex;
  justify-content: center;
  flex-direction: column;
  border-left: 1px solid #ddd;
  border-right: 1px solid #ddd;
  transition: 0.5s all ease;
}
</style>
