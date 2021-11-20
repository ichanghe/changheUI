<template>

 <router-view />
</template>

<script>
// import { ref } from '@vue/reactivity'
import { provide , ref} from 'vue'
// import HelloWorld from './components/HelloWorld.vue'
// import Frank from './components/Frank.vue'
export default {
  name: 'App',
  setup(){
    const menuVisible = ref(false)
    provide('menuVisible',menuVisible)
  }
}
</script>
