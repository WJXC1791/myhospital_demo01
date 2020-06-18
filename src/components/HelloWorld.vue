<template>
  <div class="hello">
    <el-form :model="ruleForm" :rules="rules" ref="ruleForm" label-width="100px" class="demo-ruleForm">
      <el-row>
        <el-col :span="5">
          <h4>{{ msg }}</h4>
        </el-col>
        <el-col :span="5">
          <el-form-item class="username" label="用户名：" prop="username">
            <el-input size="mini" v-model="ruleForm.username" placeholder="请输入用户名" clearable></el-input>
          </el-form-item>
        </el-col>
        <el-col :span="5">
          <el-form-item class="password" label="密码：" prop="password">
            <el-input size="mini" v-model="ruleForm.password" placeholder="请输入密码" show-password clearable></el-input>
          </el-form-item>
        </el-col>
        <el-col :span="8">
          <el-form-item>
            <el-button type="primary" @click="submitForm('ruleForm')" icon="el-icon-user-solid">
              <router-link to="Login.vue">登录</router-link>
            </el-button>
            <el-button type="primary" @click="onRegister" icon="el-icon-s-custom">
              <router-link to="Register.vue">注册</router-link>
            </el-button>
          </el-form-item>
        </el-col>
      </el-row>
    </el-form>
    <el-header>
      <img class="imglogo" src="../images/hospital001.jpeg"/>
      <span class="namelogo">人民医院</span>
      <img class="imglogo1" src="../images/hospitalplaza004.jpeg" align="right"/>
    </el-header>
    <el-main class="mainmenu">
      <el-row :gutter="24">
        <el-col :span="3"><div class="grid-content bg-purple"><a href="">首页</a></div></el-col>
        <el-col :span="3"><div class="grid-content bg-purple">医院简介</div></el-col>
        <el-col :span="3"><div class="grid-content bg-purple">医院动态</div></el-col>
        <el-col :span="3"><div class="grid-content bg-purple">科室设置</div></el-col>
        <el-col :span="3"><div class="grid-content bg-purple"><a href="/doctor">名医精粹</a></div></el-col>
        <el-col :span="3"><div class="grid-content bg-purple">医疗服务</div></el-col>
        <el-col :span="3"><div class="grid-content bg-purple">医学中心</div></el-col>
        <el-col :span="3"><div class="grid-content bg-purple">联系我们</div></el-col>
      </el-row>
    </el-main>
  </div>
</template>

<script>
  export default {
    name: 'HelloWorld',
    data () {
      return {
        msg: '欢迎访问人民医院官方网站',
        ruleForm: {
          username: '',
          password: ''
        },
        rules: {
          username: [
            { required: true, message: '请输入用户名', trigger: 'blur' },
          ],
          password: [
            { required: true, message: '请输入密码', trigger: 'blur' }
          ]
        },
        activeIndex: '1',
        activeIndex2: '1'
      }
    },
    methods: {
      submitForm(ruleForm) {
        this.$refs[ruleForm].validate((valid) => {
          if (valid) {
            alert('submit!');
          } else {
            console.log('error submit!');
            return false;
          }
        });
      },
      handleSelect(key, keyPath) {
        console.log(key, keyPath);
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  /*.demo-ruleForm {*/
  /*  margin-left: 25px;*/
  /*}*/
  h4 {
    font-weight: normal;
    left: 260px;
  }
  a {
    color: #fff;
  }
  .username, .password {
    text-align: right;
  }
  .namelogo {
    margin-left: 100px;
    height: 50px;
    font-weight: bold;
    font-size: 60px;
  }
  .imglogo {
    height: 150px;
    width: auto;
  }
  .imglogo1 {
    height: 150px;
    width: auto;
  }
  .mainmenu {
    margin-top: 100px;
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
  .bg-purple {
    background: #d3dce6;
  }
  .bg-purple-light {
    background: #e5e9f2;
  }
  .grid-content {
    border-radius: 4px;
    min-height: 36px;
    text-align: center;
  }
  .row-bg {
    padding: 10px 0;
    background-color: #f9fafc;
  }
</style>
