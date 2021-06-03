<template>
  <div id="home">
    <nav-bar class="home-nav"><div slot="center">购物车</div></nav-bar>
    <home-swiper :banners="banners" />
    <recommend-view :recommends="recommends" />
    <feature-view />
    <ul>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
      <li>{fsdfds}</li>
    </ul>
  </div>
</template>

<script>
  import NavBar from 'components/common/navbar/NavBar';
  import HomeSwiper from './childComps/HomeSwiper'
  import RecommendView from './childComps/RecommendView'
  import FeatureView from './childComps/FeatureView'

  import {getHomeMultidata} from "network/home";

  export default {
    name: "Home",
    components: {
      NavBar,
      HomeSwiper,
      RecommendView,
      FeatureView
    },
    data() {
      return {
        banners: [],
        recommends: [],
      }
    },
    created() {
      getHomeMultidata().then(res => {
        console.log(res);
        this.banners = res.data.banner.list;
        this.recommends = res.data.recommend.list;
      })
    }
  }
</script>

<style scoped>
  #home {
    padding-top: 44px;
  }

  .home-nav {
    background-color: var(--color-tint);

    position: fixed;
    left: 0;
    right: 0;
    top: 0;
    z-index: 9;
  }
</style>
