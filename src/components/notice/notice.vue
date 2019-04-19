<template>
  <div>
    <div>
      <button @click="handleback()">返回</button>
      <span>通知</span>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  methods: {
    handleback() {
      this.$router.back();
    }
  }
};
</script>

<style scoped>
</style>

