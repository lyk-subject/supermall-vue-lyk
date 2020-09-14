<!--  -->
<template>
  <div>
    <nav-bar class="nav-bar-center">
      <div slot="center">购物街</div>
    </nav-bar> 
    <field/>
    <swiper :banner="banner"></swiper>
  </div>
</template>

<script>
import NavBar from "components/common/navbar/NavBar";
import Swiper from "components/common/swiper/Swiper";
import Field from "components/common/field/Field";
//不是default导出的
import { getHomeMultidata } from "network/home";
export default {
  data() {
    return {
      banner: [],
      recommend: [],
    };
  },
  components: {
    NavBar,
    Swiper,
    Field
  },
  created() {
    //1.请求多个数据
    getHomeMultidata().then((res) => {
      this.banner = res.data.banner.list;
      this.recommend = res.data.recommend.list;
    });
  },
};
</script>

<style  scoped>
.nav-bar-center {
  background: var(--color-tint);
  color: white;
}
</style>
