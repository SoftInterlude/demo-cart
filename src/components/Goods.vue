<template>
  <div class="goods-item">
    <img class="goods-img" src="../assets/logo.png" alt="" />
    <div class="goods-desc">
      <div class="goods-title">
        <a href="#">
          班俏BANQIAO超火ins潮卫衣女士2020秋季新款韩版宽松慵懒风薄款外套带帽上
        </a>
      </div>
      <div class="goods_count">
        <Counter></Counter>
      </div>
    </div>
  </div>
</template>

<script>
import Counter from "@/components/Counter.vue";

export default {
  props: {
    id: {
      type: Number,
      required: true,
    },
    goods_name: {
      type: String,
      required: true,
    },
    goods_img: {
      type: String,
      required: true,
    },
    goods_count: {
      type: Number,
      default: 1,
    },
    goods_price: {
      type: Number,
      required: true,
    },
  },
  components: {
    Counter,
  },
};
</script>

<style lang="less" scoped>
a {
  text-decoration: none;
  color: #000;
}

.goods-item {
  width: 100%;
  overflow: hidden;
  .goods-img {
    float: left;
    width: 125px;
    vertical-align: center;
  }
  .goods-desc {
    float: right;
    width: calc(100% - 125px);
    height: 125px;
    .goods-title,
    .goods-count {
      float: right;
    }
    font-size: 14px;
    text-overflow: ellipsis;
    overflow-x: hidden;
  }
}

.goods-item::before,
.goods-item::after {
  content: " ";
  display: table-cell;
  clear: both;
}
</style>