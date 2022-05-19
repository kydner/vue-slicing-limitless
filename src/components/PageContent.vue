<template>
  <div class="page-content">
    <h4>{{ title }}</h4>
  </div>
</template>
<script>
export default {
  props: {
    title: {
      type: String,
      default: null,
    },
  },
};
</script>
