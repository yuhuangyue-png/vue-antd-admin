<template>
  <div>
    <a-button type="primary" @click="jumpToPublicPage">jump</a-button>
    <p>query: {{$route.query}}</p>
    <p>params: {{$route.params}}</p>
  </div>
</template>

<script>
  export default {
    name: 'Demo',
    methods:{
    jumpToPublicPage(){
      this.$router.push('/public')
    }
  }
  }
</script>

<style scoped>

</style>
