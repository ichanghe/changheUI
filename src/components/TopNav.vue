<template>
  <div>
    <div class="topnav">
      <div class="logo" @click="toggleMenu">导航栏</div>
      <div class="menu">
        <li></li>
        <li></li>
      </div>
    </div>
  </div>
</template>
<script lang="ts">
import { inject, Ref } from 'vue'
export default {
  name:'TopName',
  setup(){
    const menuVisible = inject<Ref<boolean>>('menuVisible')
    console.log(menuVisible)
    const toggleMenu = ()=>{
      menuVisible.value = !menuVisible.value
      console.log(menuVisible,'menuVisbel')
    }
    return {toggleMenu}
  }
}
</script>
<style lang="scss" scoped>
.topnav {
  background: pink;
  display: flex;
  padding: 16px;
  position: relative;
  z-index: 10;
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