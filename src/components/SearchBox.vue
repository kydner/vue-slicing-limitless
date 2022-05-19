<template>
  <div class="input-search">
    <b-icon class="input-search__icon" icon="search"></b-icon>
    <input type="text" placeholder="Search" />
  </div>
</template>
<script>
export default {};
</script>
<style lang="scss" scoped>
$icon-color: #888;
.input-search {
  position: relative;
  width: 100%;
  .input-search__icon {
    position: absolute;
    top: 50%;
    left: 0.8rem;
    transform: translateY(-50%);
    fill: $icon-color;
  }
  input {
    appearance: none;
    border-radius: 2rem;
    border: none;
    background-color: #eee;
    padding: 0.4rem 2.5rem;
    font-size: 0.9rem;
    width: 100%;
    &:focus-visible {
      outline: none;
    }
  }
}
</style>
