<script >
// import HelloWorld from './components/HelloWorld.vue'
import axios from 'axios';
import { createApp } from 'vue';

const API = "http://127.0.0.1:8000/api/z0"

export default{
  name:createApp,
  mounted(){
    axios.get(API + '/projects')
      .then(res=>{
        console.log(res.data);
      })
      .catch(err => console.error(err));
  }

}
</script>

<template>
  <h1>Aooo</h1>
</template>

<style scoped>
</style>
