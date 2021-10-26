<template>
  <div>
    <button class="button button-left">-</button>
    <span>1</span>
    <button class="button button-right">+</button>
  </div>
</template>

<script>
export default {};
</script>

<style lang="less" scoped>
.button {
  width: 20px;
  height: 20px;
  border-radius: 5px;
  background-color: #eee;
}

.button-left {
  margin-right: 5px;
}

.button-right {
  margin-left: 5px;
}
</style>