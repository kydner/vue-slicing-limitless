<template>
  <div class="sidebar-menu-list">
    <ul>
      <li v-for="(item, index) in list" :key="index">
        <span style="padding-left: 1rem">{{ item.title }}</span>
        <NestedList :list="item.children" />
      </li>
    </ul>
  </div>
</template>
<script>
import NestedList from "../components/NestedList.vue";
export default {
  components: {
    NestedList,
  },
  data() {
    return {
      list: [],
    };
  },
  mounted() {
    this.list = [
      {
        title: "Main",
        children: [
          {
            title: "Dashboard",
            subtitle: "No active orders",
            icon: "building",
          },
          {
            title: "Layouts",
            icon: "file-ruled",
            children: [
              {
                title: "Default Layout",
              },
              {
                title: "Layout 2",
              },
            ],
          },
        ],
      },
      {
        title: "Layout",
        children: [],
      },
    ];
  },
};
</script>
<style lang="scss" scoped>
.sidebar-menu-list {
  ul {
    list-style: none;
    margin: 0;
    padding: 0;
    color: #ccc;
    text-transform: uppercase;
    font-size: 0.8rem;
    // li {
    //   padding: 0.5rem 1rem;
    // }
  }
}
</style>
