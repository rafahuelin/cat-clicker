<template>
  <div>
    <h1>{{this.counterValue}}</h1>
  </div>
</template>

<script>
export default {
  name: 'Scoreboard',
  props: ['counterValue']
}
</script>

<style scoped>
div {
  width: 150px;
  border: 4px solid black;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
