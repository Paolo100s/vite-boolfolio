<script >
// import HelloWorld from './components/HelloWorld.vue'
import axios from 'axios';
import ProjectCard from '../components/ProjectCard.vue';


const API = "http://127.0.0.1:8000/api/z0"

export default{
  name: 'AppHome',
  components:{
    ProjectCard
  },
  data() {
    return {
      projects: []
    }
  },
  mounted(){
    axios.get(API + '/projects')
      .then(res=>{
        this.projects=res.data.projects;
      })
      .catch(err => console.error(err));
  }

}
</script>

<template>
    <div class="row">
        <ProjectCard v-for="project in projects" :key="project.id" :project="project"/>
    </div>
</template>
  
  <style scoped>
  .row{
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
  }
  </style>