<template>
  <img class="image" alt="Vue logo" src="./assets/logo.png">
  <PersonList/>
</template>

<script>
import PersonList from './components/PersonList.vue'

export default {
  name: 'App',
  components: {
    PersonList
  }
}
</script>

<style>
.image{
  margin: 0 auto 0 auto;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

*{
  margin: 0;
  padding: 0;
}
</style>
