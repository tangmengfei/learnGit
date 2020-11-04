<template>
  <div class="login_container">
    <div class="login_box">
      <div class="avatar_box">
        <img src="../assets/logo.png">
      </div>
      <div>
        <el-form ref="loginForm" :model="loginForm" label-width="80px" class="login_form">
          <el-form-item label="账户:">
            <el-input v-model="loginForm.username"/>
          </el-form-item>
        </el-form>
      </div>
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
    background-image: url("../assets/image/login/login_nanjing.jpg");
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
      border: 1px solid #eeeeee;
      border-radius: 50%;
      padding: 10px;
      box-shadow: 0 0 10px #dddddd;
      position: absolute;
      left: 50%;
      transform: translate(-50%, -50%);
      background-color: #ffffff;
      img{
        height: 100%;
        width: 100%;
        border-radius: 50%;
        background-color: #eeeeee;
      }
    }
  }
  .login-form{
    border-radius: 6px;
    background: #ffffff;
    width: 400px;
    /*padding: 25px 25px 5px 25px;*/
    position: absolute;
    top: 50%;
  }
</style>
