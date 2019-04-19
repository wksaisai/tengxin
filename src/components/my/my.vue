<template>
  <div class="my">
    <div class="head">
      <h2>我的</h2>
      <router-link to="/notice">
        <i class="iconfont">&#xe677</i>
      </router-link>
    </div>
    <div class="info">
      <div class="info-show">头像</div>
      <div>
        <span>王笑笑</span>
        <p>13800000000</p>
      </div>
    </div>
    <div class="list">
      <ul>
        <li v-for="(item,index) in list" :key="index">
          <router-link :to="item.path">
            <div>
              <i></i>
              <span>{{item.con}}</span>
            </div>
          </router-link>
        </li>
      </ul>
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
      list: [
        {
          path: "/form",
          img: "哈哈",
          con: "数据统计"
        },
        {
          path: "/plan",
          img: "呵呵",
          con: "巡检计划"
        }
      ]
    };
  }
};
</script>


<style scoped>
.my > .head {
  border-bottom: 1px solid black;
  display: flex;
  justify-content: space-between;
}
.my > .info {
  display: flex;
}
.my > .info > .info-show {
  border: 1px solid black;
  width: 0.8rem;
  height: 0.8rem;
  border-radius: 50%;
  text-align: center;
  line-height: 0.8rem;
}
</style>