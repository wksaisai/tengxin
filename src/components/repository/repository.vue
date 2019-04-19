<template>
  <div class="repository">
    <div class="head">
      <h2>知识库</h2>
      <router-link to="/notice">
        <i class="iconfont">&#xe677</i>
      </router-link>
    </div>
    <div class="content">
      <div @click="handleto()">桌面云</div>
      <div @click="handleto()">液位仪</div>
      <div @click="handleto()">加管云</div>
      <div @click="handleto()">加油机</div>
      <div @click="handleto()">服务器</div>
      <div @click="handleto()">电脑</div>
    </div>
    <Footer-com/>
  </div>
</template>

<script>
import Footer from "../common/footer";
export default {
  components: {
    "Footer-com": Footer
  },
  data() {
    return {
      handleto() {
        this.$router.push("/book");
      }
    };
  }
};
</script>


<style scoped>
.repository {
  width: 100%;
  height: 100%;
}
.repository > .head {
  border-bottom: 1px solid black;
  display: flex;
  justify-content: space-around;
}
.repository > .content {
  /* display: flex; */
  /* justify-content: space-around; */
}
.repository > .content > div {
  width: 3rem;
  float: left;
  height: 2rem;
  border: 1px solid black;
  margin: 0.15rem;
}
</style>