<template>
  <div class="loginContainer">
    <Logo />
    <div class="loginLeft">
      <img src="../../assets/img/loginLeft.png" style="width: 80%" />
    </div>
    <div class="loginRight">
      <div class="LanguagesSwitchContainer">
        <LanguagesSwitch />
      </div>
      <LoginForm />
    </div>

    <div class="copyRight">
      <a href="https://modernwms.ikeyly.com" target="_blank">CopyRight © 2023 ModernWMS All Rights Reserve</a>
    </div>
    <div class="ICP" @click="method.toICP"> 闽ICP备2021008548号 </div>
  </div>
  <div class="loginBg">
    <div class="loginContent">
      <div class="loginContentBox">
        <div class="loginImage">
          <img src="../../assets/img/loginImage.jpg" />
        </div>
        <div class="loginFormWrapper">
          <div class="auth-form-wrapper">
            <LoginForm />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { reactive } from 'vue'
import LoginForm from '@/components/login/login-form.vue'
import LanguagesSwitch from '@/components/system/languages.vue'
import Logo from '@/components/system/logo.vue'

const method = reactive({
  toICP: () => {
    window.open('https://beian.miit.gov.cn/', '_blank')
  }
})
</script>

<style scoped lang="less">
.LanguagesSwitchContainer {
  position: absolute;
  right: 10px;
  top: 10px;
}
.loginContainer {
  width: 100%;
  height: 100%;
  display: flex;
  background-color: #fff;
  position: relative;
  .loginLeft {
    width: 70%;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .loginRight {
    width: 30%;
    background-color: #fafafa;
    display: flex;
    align-items: center;
  }
}

.copyRight {
  width: 100%;
  color: #bbb;
  display: flex;
  justify-content: center;
  font-size: 12px;
  position: absolute;
  bottom: 30px;
  left: 50%;
  transform: translate(-50%, -50%);
}

.ICP {
  color: #999;
  font-size: 12px;
  position: absolute;
  bottom: 10px;
  left: 50%;
  transform: translate(-50%, -50%);

  &:hover {
    cursor: pointer;
    color: #aaa;
  }
}
.loginBg{
  background: #070d19;
  height: 100vh;
}
.loginContent{
  color: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%
}
.loginContentBox{
  display: flex;
  justify-content: center;
}
.loginImage{
  width: 20%;
  object-fit: cover;
    overflow: hidden;
    border-top-left-radius: 4px;
    border-bottom-left-radius: 4px;
}
.loginImage img{
  height: 100%;
}
.loginFormWrapper{
    background: #0c1427;
  border: 1px solid #172340;
  border-top-right-radius: 4px;
    border-bottom-right-radius: 4px;
}
.auth-form-wrapper{
  
}
</style>
