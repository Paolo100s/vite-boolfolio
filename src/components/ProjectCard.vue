<script>
export default{
    props:{
        project:{
            type: Object
        }
    }
}
</script>

<template>
    <div class="card">
        <h2>{{ project.name }}</h2>
        <p>{{ project.description }}</p>
        <span>{{ project.difficulty }}</span>
    </div>
</template>

<style scoped>
.card {
    width: 30%;
    border: 1px solid black;
    margin-bottom: 30px;
}   
</style>