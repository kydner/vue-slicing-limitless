<template>
  <div id="app">
    <!-- <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </nav> -->
    <Header />
    <Sidebar />
    <div class="main">
      <router-view />
    </div>
  </div>
</template>
<script>
import Header from "./components/app/Header.vue";
import Sidebar from "./components/app/Sidebar.vue";
export default {
  components: {
    Header,
    Sidebar,
  },
};
</script>
<style>
/* @import "./assets/scss/main.scss"; */
</style>
