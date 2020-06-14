<template>
  <div class="hello">
    <h4>{{ msg }}</h4>
    <el-form ref="form" :model="form" label-width="80px">
      <el-form-item class="username" label="用户名：">
        <el-input v-model="form.username" placeholder="请输入用户名" clearable></el-input>
      </el-form-item>
      <el-form-item label="密码：" class="password">
        <el-input v-model="form.password" placeholder="请输入密码" show-password clearable></el-input>
      </el-form-item>
      <el-form-item>
        <el-button type="primary" @click="onSubmit">
          <a href="./src/components/Login.vue">登录</a>
        </el-button>
      </el-form-item>
    </el-form>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: '欢迎访问市人民医院官方网站',
      form: {
        username: '',
        password: ''
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h4 {
    font-weight: normal;
    left: 200px;
  }
  a {
    color: #fff;
  }
</style>
