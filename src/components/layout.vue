<!--compontens下放公共的组件pages下放路由页面-->
<template>
  <div class="content">
      <div class="app-header">
          <img src="../assets/logo.png" alt="logo">
          <div class="head-nav">
              <ul class="nav-list">
                  <li>登录</li>
                  <li class="nav-pile">|</li>
                  <li>注册</li>
                  <li class="nav-pile">|</li>
                  <li>关于</li>
              </ul>
          </div>
      </div>
      <div class="app-content">
          <keep-alive>
            <router-view></router-view>
          </keep-alive>
      </div>
      <!-- <div class="app-foot">wzy 504706316@qq.com</div> -->
  </div>
</template>

<script>
export default {
  data () {
      return {}
  }
}
</script>

<style>
*{
    margin: 0;
    padding: 0;
 }

li{
    list-style: none;
}

html,body,.content{
    height: 100%;
    width: 100%;
    background-color: #d1d1ce;
    
}

.app-header{
    background: #363636;
    color: #b2b2b2;
    height: 60px;
    width: 100%;
 }

.app-header img{
    width: 50px;
    margin: 5px 0 0 15px;
}

.head-nav{
    float: right;
    margin:10px 20px;
}

.nav-list li{
    cursor: pointer;
    float: left;
}

.nav-pile {
  padding: 0 10px;
}

.app-foot {
  text-align: center;
  height: 50px;
  width: 100%;
  line-height: 50px;
  background: #e3e4e8;
  clear: both;
  /* margin-top: 30px; */
}

.app-content{
    /* overflow: hidden; */
    
}
</style>
