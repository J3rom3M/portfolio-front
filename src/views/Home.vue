<template>
  <div class="home">
    <img alt="Picture of me" src="../assets/Moi.jpg">
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
