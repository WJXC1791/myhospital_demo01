<template>
  <div class="hello">
    <el-form :model="ruleForm" :rules="rules" ref="ruleForm" label-width="100px" class="demo-ruleForm">
      <el-row>
        <el-col :span="8">
          <h4>{{ msg }}</h4>
        </el-col>
        <el-col :span="8">
          <el-form-item class="username" label="用户名：" prop="name">>
            <el-input v-model="ruleForm.username" placeholder="请输入用户名" clearable></el-input>
          </el-form-item>
        </el-col>
        <el-col :span="8">
          <el-form-item class="password" label="密码：" prop="password">
            <el-input v-model="ruleForm.password" placeholder="请输入密码" show-password clearable></el-input>
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
      <img class="imglogo1" src="../images/hospitalplaza001.jpeg"/>
      <img class="imglogo1" src="../images/hospitalplaza002.jpeg"/>
      <img class="imglogo1" src="../images/hospitalplaza003.jpeg"/>
      <img class="imglogo1" src="../images/hospitalplaza004.jpeg"/>
    </el-header>
  </div>
</template>

<script>
  export default {
    name: 'HelloWorld',
    data () {
      return {
        msg: '欢迎访问市人民医院官方网站',
        ruleForm: {
          username: '',
          password: ''
        },
        // rules: {
        //   name: [
        //     { required: true, message: '请输入用户名', trigger: 'blur' },
        //   ],
        //   region: [
        //     { required: true, message: '请输入密码', trigger: 'blur' }
        //   ]
        // }
      }
    },
    // methods: {
    //   submitForm(ruleForm) {
    //     this.$refs[ruleForm].validate((valid) => {
    //       if (valid) {
    //         alert('submit!');
    //       } else {
    //         console.log('error submit!');
    //         return false;
    //       }
    //     });
    //   }
    // }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h4 {
    font-weight: normal;
    left: 260px;
  }
  a {
    color: #fff;
  }
  .username, .password {
    text-align: right;
    height: 10px;
    width: 300px;
  }
  .imglogo {
    text-align: left;
    height: 150px;
    width: auto;
  }
  .imglogo1 {
    text-align: right;
    height: 150px;
    width: auto;
  }
</style>
