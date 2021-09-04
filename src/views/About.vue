<template>
  <div class="about">
    <h1>À propos de moi-même :</h1>
    <p>Jérôme Magnier - Développeur web fullstack (PHP - Symfony - Vue.JS)</p>
    <img alt="Me" src="../assets/Moi.jpg" id="me">
  </div>
</template>

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
  background-color: #0f056b;
  height: 100em;
  margin: 1%;
}

#me {
  position:absolute;
  top:20px;
  right:20px;
}

</style>