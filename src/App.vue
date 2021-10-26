<template>
  <div id="app">
    <!-- 头部区域 -->
    <Header></Header>
    <!-- 购物车列表区域 -->
    <main class="cart-main">
      <div class="cart-main-space"></div>
      <Goods></Goods>
      <Goods></Goods>
      <Goods></Goods>
    </main>
    <!-- 底部区域 -->
    <Footer></Footer>
  </div>
</template>

<script>
import axios from "axios";
import Header from "@/components/Header.vue";
import Footer from "@/components/Footer.vue";
import Goods from "@/components/Goods.vue";

export default {
  name: "App",
  components: {
    Header,
    Footer,
    Goods,
  },
  methods: {
    async getInitialList() {
      const { data: req } = await axios.get("https://www.escook.cn/api/cart");
      console.log(req);
    },
  },
  mounted() {
    this.getInitialList();
  },
};
</script>

<style lang="less">
* {
  padding: 0;
  margin: 0;
}

#app {
  position: relative;
  margin: 0 auto;
  max-width: 540px;
  min-width: 360px;
  height: 667px;
  .cart-ctrl {
    background-color: blue;
    height: 40px;
    line-height: 40px;
    font-size: 16px;
    color: #fff;
    font-weight: 700;
  }
  .cart-header {
    width: 100%;
    position: fixed;
    text-align: center;
  }
  .cart-main {
    // margin-top: 50px;
    .cart-main-space {
      height: 50px;
    }
  }
  .cart-footer {
    width: 100%;
    position: fixed;
    left: 0;
    bottom: 0;
    // transform: translateY(-50%);
    .cart-footer-count {
      float: left;
      padding-left: 50px;
    }
    .cart-footer-count {
      float: right;
      padding-right: 30px;
    }
  }
}
</style>
