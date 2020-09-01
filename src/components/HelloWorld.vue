<template>
  <div class="hello">
    <h2>Custom Message</h2>
    <div>
      <button @click="successMessage">success</button>
      <button @click="errorMessage">error</button>
      <button @click="warnMessage">warn</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  methods: {
    successMessage() {
      this.$message({
        type: 'success',
        message: '操作成功',
        duration: '2000',
      })
    },
    errorMessage() {
      this.$message({
        type: 'error',
        message: '操作失败',
        duration: '2000',
      })
    },
    warnMessage() {
      this.$message({
        type: 'warn',
        message: '异常警告',
        duration: '2000',
      })
    },

  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
