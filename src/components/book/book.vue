<template>
  <div>
    <div class="head">
      <button @click="handleback()">返回</button>
      <h2>液位仪</h2>
    </div>
    <div class="content">
        <h2>液位仪故障了怎么办？来找答案</h2>
        <p>
            我来告诉你
            <br>
            我来告诉你
            <br>
            我来告诉你
            <br>
            我来告诉你
            <br>
            我来告诉你
            <br>
            我来告诉你
        </p>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    handleback() {
      this.$router.back();
    }
  }
};
</script>

<style scoped>
.head{
    display: flex;
    justify-content: space-around;
    border-bottom: 1px solid black;
}
</style>