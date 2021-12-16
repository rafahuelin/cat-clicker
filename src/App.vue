<template>
  <div>
    <h1>Cat-Clicker</h1>
    
    <div class="container">
      <CatList :cats="cats" @select-cat="i => activeCatIdx = i" />
      <ClickCounter :cat="cats[activeCatIdx]" v-on:count-click="increaseCounter" />
    </div>
  </div>
</template>

<script>
import ClickCounter from './components/ClickCounter.vue'
import CatList from './components/CatList.vue'

export default {
  name: 'App',
  components: {
    ClickCounter,
    CatList,
  },
  data() {
    return {
      activeCatIdx: 0,
      cats: [
        {
          name: 'Top Cat',
          imgName: 'topcat.gif',
          count: 0
        },
        {
          name: 'Benny the Ball',
          imgName: 'benny_the_ball.jpg',
          count: 0
        },
        {
          name: 'Choo-Choo',
          imgName: 'choo-choo.jpg',
          count: 0
        },
        {
          name: 'Brain',
          imgName: 'brain.jpg',
          count: 0
        },
        {
          name: 'Fancy-Fancy',
          imgName: 'fancy-fancy.jpg',
          count: 0
        },
        {
          name: 'Spook',
          imgName: 'spook.jpg',
          count: 0
        },
      ]
    }
  },
  methods: {
    increaseCounter() {
      this.cats[this.activeCatIdx].count += 1
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  margin-right: auto;
  margin-left: auto;
  text-align: center;
  width: 800px;
}

.container {
  display: flex;
  justify-content: space-around;
}
</style>
