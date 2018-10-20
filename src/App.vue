<template>
  <div id="app">
    <img src="./assets/logo.png">
    <HelloWorld v-if="isShow"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data() {
    return {
      isShow: true
    };
  },
  mounted() {
    setInterval(() => {
      this.isShow = !this.isShow;
    }, 1000);
  },
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
</style>
