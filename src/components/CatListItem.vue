<template>
  <div @click="$emit('select-cat', idx)">{{cat.name}}</div>
  <span>{{index}}</span>
</template>

<script>
export default {
  name: 'CatListItem',
  props: ['cat', 'idx']
}
</script>

<style scoped>
  div {
    border: 4px blueviolet solid;
    margin-bottom: 10px;
    padding: 10px;
    width: 150px;
  }

  div:hover {
    border-color: greenyellow;
    cursor: pointer;
  }
</style>