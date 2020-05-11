<template>
  <div class="page-login">
    <header class="login-header">
      <a class="logo" href="http://www.meituan.com"></a>
    </header>
    <div class="login-panel">
      <div class="banner">
        <img
          src="//s0.meituan.net/bs/file/?f=fe-sso-fs:build/page/static/banner/www.jpg"
          width="480"
          height="370"
          alt="美团网"
        />
      </div>
      <div class="form">
        <h4 v-if="error" class="tips">{{error}}</h4>
        <p>
          <span class="loginWord">账号登陆</span>
        </p>
        <el-input placeholder="手机号" v-model="userName"  prefix-icon="profile"></el-input>

        <el-input placeholder="密码" v-model="password" prefix-icon="password" show-password></el-input>
       <p>
          <em>忘记密码?</em>
       </p>
       <el-button type="primary" class="btn-login" @click="submit">登录</el-button>
       <p class="reg">还没有账号？ <a>免费注册</a></p>
       <div class="oauth-wrapper J-oauth-wrapper">
            <h3 class="title-wrapper"><span class="title">用合作网站账号登录</span></h3>
            <div class="oauth cf">
                <span class="oauth__link oauth__link--qq third-login-btn" data-href="/account/connect/tencent" target="_blank" id="J-third-tencent"></span>
                <span class="oauth__link oauth__link--weibo third-login-btn" data-href="/account/connect/sina" target="_blank" id="J-third-sina"></span>
            </div>
            <i id="thirdLoginRiskpartner" data-riskpartner="0"></i>
        </div>
      </div>
    </div>
    <footer class="footer">
    <div class="site-info-nav cf">
        <ul>
            <li class="first"><a rel="nofollow" href="https://about.meituan.com/about.html">关于美团</a></li>
            <li><a rel="nofollow" href="https://zhaopin.meituan.com/">加入我们</a></li>
            <li><a rel="nofollow" href="http://emis.meishi.meituan.com/merchantsSettled">商家入驻</a></li>
            <li><a rel="nofollow" href="https://www.meituan.com/help/faq">帮助中心</a></li>
            <li class="last"><a href="http://meituan.com/mobile">美团手机版</a></li>
        </ul>
    </div>
    <div class="copyright">
        <p>
            ©<span>2020</span>
            <a href="https://www.meituan.com">美团网团购</a>
            meituan.com
            <a href="http://www.miibeian.gov.cn/" target="_blank">京ICP证070791号</a>
            京公网安备11010502025545号
        </p>
    </div>
</footer>
  </div>
</template>

<script>
import api  from '@/api/index.js'
import axios from 'axios'
export default {
  data(){
    return {
      userName: '',
      password: '',
      error: ''
    }
  },
  created(){
    // axios.get('http://open.duyiedu.com/api/meituan/login',{
    //     params: {
    //       appkey: 'zhaolixiang_1581772005468',
    //       userName: 'sunyanting',
    //       password: '123456'
    //     }
    //   }).then(function (response) {
    //   console.log(response);
    //   })
  },
  methods: {
    submit(){
      if(!this.userName){
        this.error='请输入账号';
        return ;
      }
      if(!this.password){
        this.error='请输入密码';
        return ;
      }
      console.log(api.login)
      api.login({
        params: {
          userName: this.userName,
          password: this.password
        }
      }).then(res => {
        if(res.data.status == 'success'){
          this.$router.push({name: 'index'});
          this.$store.commit('setUserName',this.userName);
        }else{
          this.error = res.data.msg;
        }
      })
    }
  }
};
</script>
<style lang="scss">
@import "@/assets/css/login/index.scss";
</style>
