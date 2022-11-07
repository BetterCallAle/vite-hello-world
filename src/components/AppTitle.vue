<script>
export default{
    data(){
        return{
            myTitle: "La mia prima app con Vite"
        }
    }
}
</script>

<template>
    <h1>{{ myTitle }}</h1>
</template>

<style scoped>
    h1{
        color: red;
        font-size: 3rem;
        margin-top: 1rem;
        margin-left: 2rem;
    }
</style>