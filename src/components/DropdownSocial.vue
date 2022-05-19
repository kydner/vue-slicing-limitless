<template>
  <div class="dropdown-social">
    <button class="dropdown-button">
      <b-icon icon="grid-fill" scale="1.1"></b-icon>
    </button>
    <div class="dropdown-social__menu">
      <ul>
        <li>
          <div><b-icon icon="github"></b-icon><span> Github</span></div>
        </li>
        <li>
          <div><b-icon icon="github"></b-icon><span> Github</span></div>
        </li>
        <li>
          <div><b-icon icon="github"></b-icon><span> Github</span></div>
        </li>
        <li>
          <div><b-icon icon="github"></b-icon><span> Github</span></div>
        </li>
        <li>
          <div><b-icon icon="github"></b-icon><span> Github</span></div>
        </li>
        <li>
          <div><b-icon icon="github"></b-icon><span> Github</span></div>
        </li>
      </ul>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style lang="scss" scoped>
.dropdown-social {
  position: relative;
  margin: 0;
  padding: 0;
}
.dropdown-social__menu {
  position: absolute;
  display: none;
  // bottom: -8.7rem;
  right: 0;
  background-color: white;
  border-radius: 2px;
  border: solid 1px #ddd;
  min-width: 25rem;
  padding: 0;
  margin: 0;
  margin-top: 2px;
  ul {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
    padding: 0.5rem;
    // gap: 0.5rem;
    li {
      // padding: 2.5rem 2.5rem;
      margin: 0;
      flex-basis: 33.33%;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 2rem;
      div {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        gap: 0.5rem;
      }
      &:hover {
        background-color: #eee;
        // color: #fff;
      }
      svg {
        width: 1.5rem;
        height: 1.5rem;
      }
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
  padding: 1.2rem 1.25rem;
  cursor: pointer;
  &:hover {
    background-color: #eee;
  }
  &:focus-within ~ .dropdown-social__menu {
    display: block;
  }
}
</style>
