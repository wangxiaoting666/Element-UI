<template>
  <div>
    <el-button @click="show = !show">点击按钮</el-button>
    <div style="display: flex; margin-top: 20px; height: 100px;">
      <transition name="el-fade-in-linear">
        <div v-show="show" class="transition-box">我会消失在人海之中</div>
      </transition>
    </div>
  </div>
</template>
<script>
    export default {
    data: () => ({
      show: true
    })
  }
</script>
<style>
  .transition-box {
    margin-bottom: 10px;
    width: 300px;
    height: 100px;
    border-radius: 4px;
    background-color: #42B983;
    text-align: center;
    color: #fff;
    padding: 40px 20px;
    box-sizing: border-box;
    margin-left: 520px;
  }
</style>
