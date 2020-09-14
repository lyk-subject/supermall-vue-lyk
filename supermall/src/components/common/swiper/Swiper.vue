
<!--  -->
<template>
  <div>
    <van-swipe class="swipe" :autoplay="3000" indicator-color="white">
      <van-swipe-item v-for="(item, index) in banner" :key="index">
        <img :src="item.image" />
      </van-swipe-item>
    </van-swipe>
  </div>
</template>
 
<script>
import Vue from "vue";
import { Swipe, SwipeItem } from "vant";

Vue.use(Swipe);
Vue.use(SwipeItem);

export default {
  data() {
    return {};
  },
  props: {
    //props是对象时prop必须是对象，是数组时是字符串
    banner: {},
  },
  components: {},
  created() {},
};
</script>

<style  scoped>
.swipe {
  margin-bottom: 5px;
  border-radius: 7px;
  box-shadow: 10px 10px 5px rgb(75, 75, 75, 0.4);
}
.swipe .van-swipe-item {
  text-align: center;
}
img {
  width: 100%;
}
</style>
