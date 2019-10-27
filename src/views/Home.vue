<template>
  <div class="home">
    <HelloWorld msg="This is an home page" />
    <div ref="www">{{title}}</div>
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
      route: this.$route,
      age: 27
    }
  },
  created () {
    console.log(this.$route)
    console.log(this.$router)
  },
  methods: {
    handle () {
      this.title = '123'
      console.log(this.title) // 123
      console.log(this.$refs.www.innerHtml) // undefined
    }
  },
  components: {
    HelloWorld
  },
  watch: {

  }
}
</script>
