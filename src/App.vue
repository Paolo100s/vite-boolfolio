<script >
// import HelloWorld from './components/HelloWorld.vue'
// import { createApp } from 'vue';

// export default{
//   name: createApp,
// }
// BUG

import HeaderH from './components/HeaderH.vue';

export default{
  name: 'App',
  components:{
    HeaderH
  }
}

</script>

<template>
  <HeaderH/>
  <router-view/>
</template>

<style scoped>

</style>
