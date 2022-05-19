<template>
  <div class="header-search">
    <button class="button-search" @click="handleSearch">
      <b-icon icon="search"></b-icon>
    </button>
    <SearchBox style="width: 100%" />
  </div>
</template>
<script>
import { mapMutations, mapState } from "vuex";
import SearchBox from "../components/SearchBox.vue";
export default {
  components: {
    SearchBox,
  },
  data() {
    return {};
  },
  computed: {
    ...mapState({
      showSearchBox: (state) => state.app.showSearchBox,
    }),
  },
  methods: {
    handleSearch() {
      this.setShowSearchBox(!this.showSearchBox);
    },
    ...mapMutations({
      setShowSearchBox: "app/setShowSearchBox",
    }),
  },
};
</script>
