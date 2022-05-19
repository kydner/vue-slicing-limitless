<template>
  <li class="nested-list-item active">
    <div class="nested-list-item__menu">
      <b-icon :icon="item.icon"></b-icon>
      <div class="nested-list-item__title">
        <span class="title">{{ item.title }}</span>
        <span class="subtitle" v-if="item.subtitle">{{ item.subtitle }}</span>
      </div>
    </div>
  </li>
</template>
<script>
export default {
  props: {
    item: {
      type: Object,
      default: () => {},
    },
  },
};
</script>
<style lang="scss" scoped>
.nested-list-item {
  margin: 1px 0;
  .nested-list-item__menu {
    display: flex;
    align-items: center;
    gap: 1.7rem;
    padding: 1rem 0;
  }
}
.nested-list-item.active {
  background-color: #596782;
}
.nested-list-item__title {
  display: flex;
  flex-direction: column;
  .title {
    font-weight: bold;
    color: white;
  }
}
</style>
