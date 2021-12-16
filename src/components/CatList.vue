<template>
  <div class="listGroup">
    <div :key="cat.name" v-for="(cat, index) in cats">
      <CatListItem :cat="cat" :idx="index" @select-cat="i => $emit('select-cat', i)" />
    </div>
  </div>
</template>

<script>
import CatListItem from './CatListItem.vue'
export default {
  name: 'CatList',
  components: {
    CatListItem
  },
  props: ['cats']
}
</script>

<style>
</style>