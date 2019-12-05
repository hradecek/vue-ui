<template>
  <section>
    <div class="flex-1 p-16">
      <div v-masonry origin-left="true" transition-duration="1s" item-selector=".item">
        <Item />
        <Item />
        <Item />
        <Item />
        <Item />
        <Item />
        <Item />
        <Item />
      </div>
    </div>
  </section>
</template>

<script>
import Item from './Item.vue';

export default {
  name: 'mainContent',
  components: {
    Item
  }
}
</script>
