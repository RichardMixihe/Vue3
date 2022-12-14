<script>
import { ref } from 'vue';
export default {
  setup() {
    // 用什么创建什么。就像你写函数，用变量定义。用函数你定义。
    // 定义表示图片隐藏现实的标志变量
    const show = ref(true);
    // 定义函数，用来改变 show，改变页面状态
    const toggle = () => {
      show.value = !show.value;
    };
    // 计数器
    const count = ref(0);
    // 改变count的函数
    const increment = () => {
      count.value += 1;
    };

    // 把你定义的变量和函数返回给vue组件
    return { show, toggle, count, increment };
  },
};
</script>

<template>
  <img v-if="show" alt="Vite logo" src="/vite.svg" />
  <button @click="toggle">显示隐藏图片</button>
  <hr />
  <h2>计数器：{{ count }}</h2>
  <button @click="increment">累加</button>
</template>

<style scoped></style>
