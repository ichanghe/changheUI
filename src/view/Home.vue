<template>
  <div>
    <TopNav />
    <div class="banner">
      <h1>我的ui框架</h1>
      <h2>一个有用的UI框架</h2>
      <p class="actions">
        <a href="">Github</a>
        <a href="">开始</a>
      </p>
    </div>
  </div>
</template>
<script lang="ts">
import TopNav from '../components/TopNav.vue'
export default {
  components:{
    TopNav
  }
}
</script>
<style lang="scss" scoped>
.banner {
  padding: 100px 0;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  background: lightgreen;
  $h: 28px;
  > .actions{
    padding: 8px 0;
    a {
      margin:0 8px;
      background: #fff;
      display: inline-block;
      
      height: $h;
      line-height: $h;
      // border-radius: $h / 2;
      padding: 0 8px;
    }
  }
}
</style>