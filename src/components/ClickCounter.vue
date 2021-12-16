<template>
  <div>
    <h3>{{cat.name}}</h3>
    <Cat @click="$emit('count-click')" :cat="cat" />
    <Scoreboard :counterValue="cat.count" />
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
