<template>
<!--  <div id="app"></div>-->
<!--    <img src="./assets/logo.png">-->
<!--    <router-view/>-->
  <div>
    <el-header>
      <el-row>
        <el-col>
          <span class="wheader">欢迎访问市人民医院官方网站</span>
            <span class="login">
              用户名:<el-input class="username" v-model="input1" placeholder="请输入用户名" clearable></el-input>
              密码：<el-input class="password" placeholder="请输入密码" v-model="input2" show-password clearable></el-input>
            </span>
        </el-col>
      </el-row>
    </el-header>
    <el-row>
      <el-col :span="24">
        <div id="hospitallogo" class="grid-content bg-purple-dark">
          <img src="./images/hospital001.jpeg" height="100" width="100"/></div>
      </el-col>
    </el-row>
  </div>
</template>

<script>
  export default {
    name: 'App',
    data() {
      return {
        input1: '',
        input2: ''
      }
    }
  }
</script>

<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
  .el-row {
    margin-bottom: 20px;
  &:last-child {
     margin-bottom: 0;
   }
  }
  .el-col {
    border-radius: 4px;
  }
  .bg-purple-dark {
    background: #99a9bf;
  }
  .grid-content {
    border-radius: 4px;
    min-height: 36px;
  }
  .wheader {
    font-family: "Helvetica Neue", Helvetica, "PingFang SC", "Hiragino Sans GB", "Microsoft YaHei", "微软雅黑", Arial, sans-serif;
    height: 20px;
    width: auto;
  }
  .login {
    right: 10px;
  }
  .username {
    width: 200px;
    maxlength: "10";
  }
  .password {
    width: 200px;
  }
</style>
