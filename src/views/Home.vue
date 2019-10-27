<template>
  <div class="home">
    <HelloWorld msg="This is an home page" />
    <div ref="www">{{age}}</div>
    <button @click="handle">测试</button>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'home',
  data () {
    return {
      age: 27
    }
  },
  methods: {
    handle () {
      console.log(this.$refs.www.innerText)
    }
  },
  components: {
    HelloWorld
  },
  watch: {

  }
}
</script>
