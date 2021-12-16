<template>
  <div>
    <img :src="require('@/assets/img/' + cat.imgName)" :alt="cat.name">
  </div>
</template>

<script>
export default {
  name: 'Cat',
  props: ['cat']
}
</script>

<style scoped>
img {
  align-items: center;
  border: 4px solid blueviolet;
  cursor: pointer;
  display: flex;
  justify-content: center;
  width: 150px;
}

img:hover {
  border-color: yellowgreen;
}
</style>
