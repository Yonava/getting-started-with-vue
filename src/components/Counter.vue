<template>
  <div id="app">
    <p v-if="count >= 10">top secret message!</p>
    <p v-else-if="count >= 5">kinda secret message...</p>
    <p v-else>there are no secret messages</p>
    <input type="number" v-model="count">
    <br>
    <button @click="count++">Increment Count</button>
    <br>
    <button @click="count--">Decrement Count</button>
    <br>
    <button @click="double">Double Count</button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      count: 0
    }
  },
  methods: {
    double() {
      this.count *= 2
    }
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
