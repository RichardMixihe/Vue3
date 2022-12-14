<script>
import { ref } from 'vue';
export default {
  setup() {
    // 使用ref定义对象形式的响应式数据
    const obj = ref({ age: 18, name: '南波万' });

    // 修改对象形式的响应式数据
    const changeObj = () => {
      obj.value.age += 1;
      obj.value.name += '变';
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
