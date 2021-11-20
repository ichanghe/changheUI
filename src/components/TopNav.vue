<template>
  <div>
    <div class="topnav">
      <div class="logo">导航栏</div>
      <div class="menu">
        <li></li>
        <li></li>
      </div>
    </div>
  </div>
</template>
<script lang="ts">
export default {
  name:'TopName',
}
</script>
<style lang="scss" scoped>
  .topnar{border: 1px solid red;}
  
.topnav {
  background: pink;
  display: flex;
  padding: 16px;
  > .logo {
    max-width: 6em;
    margin-right: auto;
  }
  > .menu {
    display: flex;
    white-space: nowrap;
    flex-wrap: nowrap;
    > li {
      margin: 0 1em;
    }
  }
}
</style>