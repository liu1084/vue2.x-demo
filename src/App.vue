<template>
  <div id="app">
    <header-component></header-component>
    <img src="./assets/logo.png">
    <router-view/>
    <v-footer :version="v" :license="license" @onChange="handleChange"></v-footer>
  </div>
</template>

<script>

export default {
  name: 'App',
  data () {
    return {
      v: 1,
      license: 'MIT'
    }
  },
  methods: {
    handleChange (v) {
      this.v = v
    }
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
</style>
