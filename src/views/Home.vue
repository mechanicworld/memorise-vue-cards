<template>
  <div class="home">    
    <Start :test="test" />
  </div>
</template>

<script>
// @ is an alias to /src
import Start from '@/components/Start.vue'

export default {
  name: 'Home',
  data(){
    return {
      test: [
        {
          title:"I am a title 1 ",
          id:1
        },
        {
          title:"I am a title 2 ",
          id:2
        }
      ]
    }
  },
  components: {
    Start
  }
}
</script>
