<template>
  <div>
    <img src="../assets/img/topcat.gif" alt="topcats">
  </div>
</template>

<script>
export default {
  name: 'Cat',
  props: {
    msg: String
  }
}
</script>

<style scoped>
img {
  border: 4px solid blueviolet;
  width: 150px;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
