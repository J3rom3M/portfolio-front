<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div :key="index" v-for="(profiles, index) in profile">
      <h3> {{ profiles.firstName }} {{ profiles.name }} {{ profiles.title }} </h3>
    </div>
    <p>
      Ce portfolio a pour but d'autopromouvoir mon profil,<br>
      mon CV ainsi que l'ensemble des projets que j'ai appris à réaliser depuis ma reconversion
      <a href="https://j3rom3m.github.io/" target="_blank" rel="noopener">lien de mon portfolio</a>.
    </p>
    <h3>Experiences :</h3>
    <ul>
      <li><a href="https://github.com/J3rom3M" target="_blank" rel="noopener">Mon profil Github</a></li>
      <li><a href="https://www.linkedin.com/in/jerome-magnier-78120/" target="_blank" rel="noopener">Mon profil Linkedin</a></li>
    </ul>
    <h3>Diplômes et certifications :</h3>
    <ul>
      <div :key="index" v-for="(diplomas, index) in diploma">
        <li> {{ diplomas.title }} - {{ diplomas.content }} </li>
      </div>
    </ul>
    <h3>Technos :</h3>
    <ul>
      <div :key="index" v-for="(technos, index) in techno">
        <li> {{ technos.title }} - {{ technos.percentage }}% </li>
      </div>
    </ul>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      profile: null,
      diploma: null,
      techno: null,
    }
  },
  mounted() {
      axios
      .get('http://localhost:3000/api/profiles')
      .then((reponse) => {
        this.profile = reponse.data;
        console.log(this.profile)
      });
    axios
    .get('http://localhost:3000/api/diplomas')
    .then((reponse) => {
      this.diploma = reponse.data;
      console.log(this.diploma)
    });
    axios
    .get('http://localhost:3000/api/technos')
    .then((reponse) => {
      this.techno = reponse.data;
      console.log(this.techno)
    });
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
