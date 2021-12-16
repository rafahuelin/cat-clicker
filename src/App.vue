<template>
  <div>
    <h1>Cat-Clicker</h1>
    <div class="container" :key="cat.name" v-for="cat in cats">
      <ClickCounter :cat="cat" :imgPath="cat" />
    </div>
  </div>
</template>

<script>
import ClickCounter from './components/ClickCounter.vue'

export default {
  name: 'App',
  components: {
    ClickCounter
  },
  data() {
    return {
      cats: [
        {
          name: 'Top Cat',
          imgName: 'topcat.gif'
        },
        {
          name: 'Benny the Ball',
          imgName: 'benny_the_ball.jpg'
        },
      ]
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


</style>
