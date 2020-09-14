<!--  -->
<template>
  <div>
    <van-field v-model="searchText" placeholder="搜索商品" />
  </div>
</template>

<script>
import Vue from "vue";
import { Field } from "vant";

Vue.use(Field);

export default {
  data() {
    return { searchText: "" };
  },
};
</script>

<style  scoped>
</style>
