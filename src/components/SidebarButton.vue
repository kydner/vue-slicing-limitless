<template>
  <div>
    <BButton class="sidebar-menu__button" pill @click="handleSidebar">
      <b-icon
        icon="arrow-left-right"
        font-scale="1"
        aria-hidden="true"
      ></b-icon>
    </BButton>
    <BButton class="sidebar-menu__close" pill @click="handleSidebarClose">
      <b-icon icon="x" font-scale="1" aria-hidden="true"></b-icon>
    </BButton>
  </div>
</template>
<script>
import { mapMutations, mapState } from "vuex";
export default {
  computed: {
    ...mapState({
      showSidebar: (state) => state.app.showSidebar,
      smallSidebar: (state) => state.app.smallSidebar,
    }),
  },
  methods: {
    handleSidebar() {
      console.log("aaa");
      this.setSmallSidebar(!this.smallSidebar);
    },
    handleSidebarClose() {
      this.setShowSidebar(!this.showSidebar);
    },
    ...mapMutations({
      setShowSidebar: "app/setShowSidebar",
      setSmallSidebar: "app/setSmallSidebar",
    }),
  },
};
</script>
<style lang="scss" scoped>
@import "../assets/scss/_variables.scss";
i {
  fill: white;
}
.sidebar-menu__button {
  background-color: transparent;
  border: none;
  @media (max-width: $screen-md) {
    display: none;
  }
}
.sidebar-menu__close {
  display: none;
  background-color: transparent;
  border: none;
  @media (max-width: $screen-md) {
    display: block;
  }
}
</style>
