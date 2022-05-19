<template>
  <div>
    <div class="header">
      <div class="header-hamburger">
        <button @click="handleSidebarMenu">
          <b-icon icon="text-center" scale="1.4"></b-icon>
        </button>
      </div>
      <SearchHeader />
      <div class="header-menu">
        <div>
          <DropdownHeader />
        </div>
        <div>
          <DropdownNotification />
        </div>
        <div>
          <DropdownSocial />
        </div>
      </div>
    </div>
    <div v-if="showSearchBox" class="header-searchbar">
      <SearchBox />
    </div>
  </div>
</template>
<script>
import { mapMutations, mapState } from "vuex";
import SearchHeader from "../SearchHeader.vue";
import DropdownHeader from "../DropdownHeader.vue";
import DropdownNotification from "../DropdownNotification.vue";
import DropdownSocial from "../DropdownSocial.vue";
import SearchBox from "../SearchBox.vue";
export default {
  components: {
    SearchHeader,
    DropdownHeader,
    DropdownNotification,
    DropdownSocial,
    SearchBox,
  },
  data() {
    return {};
  },
  computed: {
    ...mapState({
      showSidebar: (state) => state.app.showSidebar,
      showSearchBox: (state) => state.app.showSearchBox,
    }),
  },
  methods: {
    handleSidebarMenu() {
      console.log(this.showSidebar);
      this.setShowSidebar(!this.showSidebar);
    },
    ...mapMutations({
      setShowSidebar: "app/setShowSidebar",
    }),
  },
};
</script>
