<template>
  <div
    :class="`sidebar ${showSidebar && 'slide'} ${smallSidebar && 'resize'} `"
  >
    <div class="sidebar__logo">
      <SidebarLogo />

      <SidebarButton />
    </div>
    <div class="sidebar-menu">
      <div class="sidebar__profile">
        <img
          src="https://mobirise.com/bootstrap-template/profile-template/assets/images/timothy-paul-smith-256424-1200x800.jpg"
          alt=""
        />
        <span>Test</span>
        <span class="sidebar__profile__title">Test@gmail.com</span>
      </div>
      <SidebarMenuList />
    </div>
  </div>
</template>
<script>
import SidebarLogo from "../SidebarLogo.vue";
import SidebarButton from "../SidebarButton.vue";
import { mapState } from "vuex";
import SidebarMenuList from "../SidebarMenuList.vue";
export default {
  components: {
    SidebarLogo,
    SidebarButton,
    SidebarMenuList,
  },
  computed: {
    ...mapState({
      showSidebar: (state) => state.app.showSidebar,
      smallSidebar: (state) => state.app.smallSidebar,
    }),
  },
};
</script>
