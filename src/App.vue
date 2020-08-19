<template>
  <div id="app">
    <Header />
    <Question />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Question from './components/Question.vue'

export default {
  name: 'App',
  components: {
    Header,
    Question
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
