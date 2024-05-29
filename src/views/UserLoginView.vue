<template>
  <div class="body">
    <div class="top"></div>
    <div class="header">
      <div id="title">
        <span>女仆咖啡厅</span>
      </div>
    </div>
    <div>
      <el-form ref="form" :model="form" label-width="700px" id="inputText">
        <el-form-item>
          <el-input v-model="form.nickname" placeholder="请输入账号"></el-input>
        </el-form-item>
        <el-form-item>
          <el-input v-model="form.password" placeholder="请输入密码"></el-input>
        </el-form-item>
      </el-form>
      <el-button id="loginButton">登录</el-button>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      form: {
        nickname: '',
        password: ''
      }
    }
  },
  methods: {
    onSubmit() {
      console.log('submit!');
    }
  }
}
</script>
<style scoped>
.body{
  background-image: url("../assets/nanbird.jpg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  width: 100%; /* 或者具体的宽度 */
  height: 100vh; /* 或者具体的高度 */
}
.header{
  width: 100%;
  height: 100px;
}
#loginButton{
  background-color: pink;
  margin-left: 700px;
  border-radius: 50px;
  opacity: 0.8;
  //margin-right: 100px;
}
#inputText{
  opacity: 0.8;
  margin-right: 100px;
  border-radius: 50%;
}
#title{
  color: rgba(255,20,147,0.8);
  opacity: 0.6;
  font-family: 华文琥珀,serif;
  font-size: 50px;
  margin-left: 600px;
  text-align: center;
}
.top{
  height: 200px;
}
</style>