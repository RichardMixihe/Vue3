<script>
import { reactive } from 'vue';
export default {
  setup() {
    // 使用 reactive 定义响应式数据
    const obj = reactive({ age: 18, name: 'bingo' });
    console.log(obj);
    // 修改 reactive 返回的响应式数据
    const changeObj = () => {
      obj.age = obj.age + 1;
      obj.name = obj.name + '变';
    };

    return { obj, changeObj };
  },
};
</script>
<template>
  <h2>{{ obj.age }}, {{ obj.name }}</h2>
  <button @click="changeObj">改</button>
</template>
<style scoped></style>
