<script>
export default {
  // setup 函数的执行时机和具体使用
  setup() {
    console.log('setup 执行');
    // 定义组件需要用的数据和函数
    let msg = 'hello vue3';
    const sayHi = () => {
      console.log('前', msg);
      msg = 'hello vue4';
      console.log('后', msg);
    };

    return { msg, sayHi };
  },

  beforeCreate() {
    console.log('组件before create');
  },
};
</script>

<template>
  <h2>{{ msg }}</h2>
  <button @click="sayHi">按钮</button>
</template>

<style scoped></style>
