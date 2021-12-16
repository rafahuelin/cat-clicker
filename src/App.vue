<template>
  <div>
    <h1>Cat-Clicker</h1>
    <div class="container">
      <Cat @click="increaseCounter" />
      <Scoreboard :counterValue="counter" />
    </div>
  </div>
</template>

<script>
import Cat from './components/Cat.vue'
import Scoreboard from './components/Scoreboard.vue'

export default {
  name: 'App',
  components: {
    Cat,
    Scoreboard,
  },
  data() {
    return {
      counter: 0
    }
  },
  methods: {
    increaseCounter() {
      this.counter += 1
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
}

.container {
  margin: 20px;
  width: 400px;
  margin: auto;
  display: flex;
  justify-content: space-around;
}
</style>
