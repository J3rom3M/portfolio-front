<template>
  <div class="home">
    <img alt="Picture of me" src="../assets/Moi.jpg" id="me">
    <HelloWorld msg="Bienvenue sur mon portfolio 2.0"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: 'Fira Code', monospace;
  @import url('https://fonts.googleapis.com/css2?family=Fira+Code&display=swap');
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color: #b9c5d5;
  border-radius: 10px;
  padding: 3%;
  margin: 0%;
  height: 100%;
}
html, 
body {
    margin: 0;
    padding: 0;
    background-color:rgb(29, 25, 80);
}

#nav {
  padding: 30px;
  text-align: left;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

#body{
  background-color: #542f46;
}

</style>
