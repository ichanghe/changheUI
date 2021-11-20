<template>
  <div>
    <topNav />
    <div class="content">
      <aside v-if="menuVisible">
        <h2>组件列表</h2>
        <ol>
          <li>
            <router-link to="/doc/switch">switch</router-link>
          </li>
          <li> <router-link to="/doc/switch">button</router-link></li>
          <li> <router-link to="/doc/switch">dialog</router-link></li>
          <li> <router-link to="/doc/switch">tabs</router-link></li>
          <!-- <li> <router-link to="/doc/switch"></router-link></li> -->
        </ol>
      </aside>
    </div>
    <!-- <div class="banner">
      <h1></h1>
      <h2></h2>
      <p class="actions">
        <a href="">Github</a>
        <a href="">开始</a>
      </p>
    </div> -->
  </div>
</template>
<script lang="ts">
import { inject, Ref } from 'vue'
import TopNav from '../components/TopNav.vue'
export default {
  components: {
    TopNav
  },
  setup(){
    const menuVisible = inject<Ref<boolean>>('menuVisible')
    console.log(menuVisible,'menuvisibel')
    return {
      menuVisible
    }
    console.log(menuVisible)
  }
}
</script>
<style lang="scss" scoped>
aside {
  background: lightblue;
  width: 150px;
  padding: 16px;
  position: fixed;
  top: 0;
  left: 0;
  padding-top: 70px;
  > h2 {
    margin-bottom: 4px;
  }
  > ol {
    > li {
      padding: 4px 0;
    }
  }
}
</style>