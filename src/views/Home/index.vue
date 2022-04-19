<template>
  <NavBar title="2021年深圳优质机构人气大PK" />
  <div class="logo">
    <img src="../../assets/logo.png" alt="logo" />
  </div>
  <div class="goGZH" @click="goGZH">{{ goGZHText }}</div>
  <div class="footer" @click="goLogin">GO LOGIN</div>
</template>
<script lang="ts" setup="props">
import NavBar from "../../components/navBar.vue";
import { ref } from "vue";
import { useRouter } from "vue-router";
const router = useRouter();

const goLogin = () => {
  router.push("/Login");
};

let goGZHText = ref<String>("打开小程序");
const goGZH = () => {
  window.open('weixin://dl/business/?t=XezVzIpwqIb')
};

// 测试打开淘宝
// window.location.href = 'taobao://'
</script>
<style lang="scss" scoped>
.logo {
  display: flex;
  img {
    margin: 0 auto;
  }
}
.goGZH {
  text-align: center;
  color: #9ab4cd;
  font-weight: bold;
}
.footer {
  padding-bottom: env(safe-area-inset-bottom);
  text-align: center;
  cursor: pointer;
  font-size: 16px;
  color: #ffffff;
  line-height: 50px;
  background: #9ab4cd;
  border-radius: 2px;
  height: 50px;
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
}
</style>
