<script>
import AppTitle from './components/AppTitle.vue'
import AppHero from './components/AppHero.vue'

export default{
  data(){
    return{

    }
  },
  components: {
    AppTitle,
    AppHero
  }
}
</script>

<template>
  <div class="container">
      <AppTitle/>
      <AppHero/>
  </div>
</template>

<style scoped>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.container{
  width: 80%;
  margin: 0 auto;
}

</style>