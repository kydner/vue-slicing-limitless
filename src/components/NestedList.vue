<template>
  <ul class="nested-list-main">
    <NestedItem v-for="(item, index) in list" :key="index" :item="item" />
  </ul>
</template>
<script>
import NestedItem from "../components/NestedItem.vue";
export default {
  components: {
    NestedItem,
  },

  props: {
    list: {
      type: [Array],
      default: () => [],
    },
  },
};
</script>
<style lang="scss" scoped>
.nested-list-main {
  padding: 0;
  margin: 0;
  li {
    padding: 0 1rem;
  }
}
</style>
