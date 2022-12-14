<script>
export default {
  data() {
    return {
      show: true,
      count: 0,
    };
  },
  methods: {
    toggle() {
      this.show = !this.show;
    },
    increment() {
      this.count++;
    },
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
