<template>
  <div class="dropdown-header">
    <button class="dropdown-button">
      <span>English</span>
      <b-icon icon="chevron-down" scale="0.8"></b-icon>
    </button>
    <ul class="dropdown-header__menu">
      <li>abc</li>
      <li>abc</li>
      <li>abc</li>
      <li>abc</li>
    </ul>
  </div>
</template>
<script>
export default {};
</script>
<style lang="scss" scoped>
.dropdown-header {
  position: relative;
  margin: 0;
  padding: 0;
}
.dropdown-header__menu {
  position: absolute;
  display: none;
  // bottom: -8.7rem;
  right: 0;
  background-color: white;
  border-radius: 2px;
  border: solid 1px #ddd;
  min-width: 10rem;
  list-style: none;
  padding: 0;
  margin-top: 2px;
  li {
    padding: 0.5rem 0.5rem;
    cursor: pointer;
    &:hover {
      background-color: #2196f3;
      color: #fff;
    }
  }
}

.dropdown-button {
  appearance: none;
  border: none;
  background-color: white;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 0.5rem;
  padding: 1rem 1.25rem;
  cursor: pointer;
  &:hover {
    background-color: #eee;
  }
  &:focus-within ~ .dropdown-header__menu {
    display: block;
  }
}
</style>
