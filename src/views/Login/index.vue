<template>
  <NavBar title="2022年深圳优质机构人气大PK" />
  <div class="login">
    <div class="logo">
      <img src="../../assets/logo.png" alt="logo" />
    </div>
  </div>
  <div class="footer" @click="goHome">GO HOME</div>
</template>
<script lang="ts" setup="props">
import NavBar from "../../components/navBar.vue";
import { useRouter } from "vue-router";
const router = useRouter();

const goHome = () => {
  router.push("/");
};
</script>
<style lang="scss" scoped>
.login {
  text-align: center;
}
.footer {
  text-align: center;
  margin-top: 60px;
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
