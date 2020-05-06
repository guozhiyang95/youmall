<template>
  <div id="home">
    <nav-bar class="hom-nave">
      <div slot="center">首页</div>
    </nav-bar>
    <h2>首页</h2>
  </div> 
</template>

<script>
import NavBar from '@/components/common/navbar/Navbar'
import {getHomeMultidata} from "@/network/home";
export default {
  name: 'Home',
  components: {
    NavBar
  },
  data() {
    return{
      banners: [],
      recommends: [],

      // result:null
    }
  },
  created() {
    getHomeMultidata().then(res =>{
      console.log(res);
      // this.result = res;
      this.banners = res.data.banner.list;
      this.recommends = res.data.recommend.list;
    })
  }
}
</script>

<style scoped>
  .hom-nave{
    background-color: var(--color-tint);
    color: #fff;
  }
</style>