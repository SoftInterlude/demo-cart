<template>
  <!-- 底部区域 -->
  <footer class="cart-ctrl cart-footer">
    <div class="cart-footer-count">共计9件商品</div>
    <div class="cart-footer-price">￥ 188.88</div>
  </footer>
</template>

<script>
export default {};
</script>

<style lang="less" scoped>
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
</style>