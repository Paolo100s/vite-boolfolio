<script>
import axios from 'axios';

const API_URL = "http://127.0.0.1:8000/api/z0"

export default {
    name: 'ProjectShow',
    data(){
        return{
            project:{}
        }

    },
    mounted() {
        const projectId = this.$route.params.id;
        
        axios.get(API_URL + '/projects/' + projectId)
        .then(res=>{
            const data = res.data;
            this.project = data.project;
        })
        .catch(err => console.error(err));
    }
}
</script>

<template>
    <h2>Project: {{ project.name }}</h2>
    <p>{{ project.description }}</p>
    <span>{{ project.difficulty }}</span>
</template>