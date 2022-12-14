<script>
import { ref } from 'vue';
export default {
  // 在 setup 中定义响应式数据
  setup() {
    // 定义一个age响应式数据
    const age = ref(18);
    // 修改数据的函数
    const decrement = () => {
      age.value = age.value - 1;
    };

    return { age, decrement };
  },
};
</script>

<template>
  <h2>{{ age }}</h2>
  <button @click="age++">+</button>
  <button @click="decrement">-</button>
</template>

<style scoped></style>
