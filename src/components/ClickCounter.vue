<template>
  <div>
    <h3>{{cat.name}}</h3>
    <Cat @click="increaseCounter" :cat="cat" />
    <Scoreboard :counterValue="counter" />
  </div>
</template>

<script>
import Cat from './Cat.vue'
import Scoreboard from './Scoreboard.vue'

export default {
  name: 'ClickCounter',
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
  },
  props: ['cat']
}
</script>

<style scoped>
div {
  display: flex;
  justify-content: space-around;
  margin-bottom: 25px;
}

h3 {
  display: block;
  text-align: left;
  width: 160px;
}
</style>
