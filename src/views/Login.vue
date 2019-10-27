<template>
  <div :class="{'login':setColor}">
    <h1>vue项目登录页</h1>
    <div>
      <label for="">权限类型：</label>
      <select v-model="selected">
        <option :value="index" v-for="(item,index) in user" :key="index">{{item}}</option>
      </select>
    </div>
    <button @click="changeRouter">登录</button>
  </div>
</template>

<script>
export default {
  data () {
    return {
      user: ['管理员', '操作员'],
      setColor: true,
      selected: '0'
    }
  },
  methods: {
    changeRouter () {
      if (this.selected === '0') {
        this.$router.push('/home')
      } else {
        this.$router.push('/about')
      }
    }
  }
}
</script>

<style scoped="scoped" lang="less">
  .login {
    width: 300px;
    height: 250px;
    margin: 100px auto;
    border: 1px solid #ccc;
    font-size: 14px;

    div {
      padding: 20px 0 70px 0;

      label {
        vertical-align: middle;
      }

      select {
        width: 100px;
        vertical-align: middle;
      }
    }

    button {
      width: 50px;
      height: 25px;
      cursor: pointer;
    }
  }
</style>
