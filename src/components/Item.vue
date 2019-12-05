<template>
  <div v-masonry-tile class="item">
    <img src="/img/sample_image.jpg" class="">
  </div>
</template>

<script>
export default {
  name: 'item'
}
</script>

<style scoped>
.item {
  margin: 10px;
  border: 1px solid black;
  max-width: 100px;
}
</style>