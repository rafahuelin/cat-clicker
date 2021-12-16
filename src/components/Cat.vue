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
div {
  margin-right: 20px;
}

img {
  align-items: center;
  border: 4px solid blueviolet;
  cursor: pointer;
  display: flex;
  height: auto;
  justify-content: center;
  object-fit: contain;
  width: 150px;
}

img:hover {
  border-color: yellowgreen;
}
</style>
