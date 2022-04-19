<template>
  <div class="navBar">
    <div class="left"></div>
    <div class="center">{{ title }}</div>
    <div class="right"></div>
  </div>
</template>
<script lang="ts" setup="props">
import { Toast } from "vant";
import { defineProps } from "vue";
import { useRouter } from "vue-router";
const router = useRouter();
const goHome = () => {
  router.push("/");
};

const props = defineProps({
  title: {
    type: String,
    default: "",
  },
});
</script>
<style lang="scss" scoped>
.navBar {
  display: flex;
  justify-content: center;
  align-items: center;

  height: 48px;
  line-height: 48px;
  color: #fff;
  background-color: #9ab4cd;
  .left {
  }
  .center {
  }
  .right {
  }
}
</style>
