<template>
  <div class="login_container">
    <div class="login_box">
      <div class="avatar_box">
        <img src="../assets/logo.png">
      </div>
<!--      <el-form ref="loginForm" :model="loginForm" label-width="90px" class="login-form">-->
<!--        <h3>疯狂哲学后台管理系统</h3>-->
<!--        <el-form-item label="账户:" prop="username">-->
<!--          <el-input v-model="loginForm.username" placeholder="账户"></el-input>-->
<!--        </el-form-item>-->
<!--        <el-form-item label="密码:" prop="password">-->
<!--          <el-input v-model="loginForm.password" placeholder="密码"></el-input>-->
<!--        </el-form-item>-->
<!--      </el-form>-->
    </div>
  </div>
</template>

<script>
export default {
  name: 'login',
  data () {
    return {
      loginForm: {
        username: '',
        password: ''
      }
    }
  }
}
</script>

<style lang="scss" rel="stylesheet/scss" scoped>
  .login_container {
    display: flex;
    justify-content : center;
    align-items: center;
    height: 100%;
    background-image: url("../assets/image/login-background.jpg");
    background-size: 100% 100%;
  }
  .login_box{
    width: 450px;
    height: 300px;
    background-color: #ffffff;
    border-radius: 6px;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    .avatar_box{
      height: 130px;
      width: 130px;
      img{
        height: 100%;
        width: 100%;
      }
    }
  }
  .login-form{
    border-radius: 6px;
    background: #ffffff;
    width: 400px;
    padding: 25px 25px 5px 25px;
  }
</style>
