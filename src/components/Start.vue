<template>
  <div class="hello">    
    <h1> {{test[0].id}} : {{test[0].title}}  </h1>
    <h1> {{test[1].id}} : {{test[1].title}}  </h1>
    
  </div>
</template>

<script>
export default {
  name: 'Start',
  props: {
    test: Array
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
