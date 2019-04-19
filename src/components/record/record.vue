<template>
  <div>
    <h2>记录</h2>
    <mt-navbar v-model="selected">
      <mt-tab-item id="1">进行中</mt-tab-item>
      <mt-tab-item id="2">已完成</mt-tab-item>
      <mt-tab-item id="3">已取消</mt-tab-item>
    </mt-navbar>

    <!-- tab-container -->
    <mt-tab-container v-model="selected">
      <mt-tab-container-item id="1">
        <!-- <mt-cell v-for="n in 10" :title="'内容 ' + n"/> -->
        <ul>
          <li v-for="(item,index) in list" :key="index">
            <router-link to="/detail">
              <div>
                <img src="##" alt>
                <span>{{item.name}}</span>
                <span>{{item.time}}</span>
              </div>
              <div>
                <span>故障类型：{{item.class}}</span>
                <span>服务时间：{{item.time2}}</span>
                <span>故障单号：{{item.num}}</span>
              </div>
            </router-link>
          </li>
        </ul>
      </mt-tab-container-item>

      <mt-tab-container-item id="2">
        <ul>
          <li v-for="(item,index) in list" :key="index">
            <!-- <router-link to="/detail"> -->
              <div>
                <img src="##" alt>
                <span>{{item.name}}</span>
                <span>{{item.time}}</span>
              </div>
              <div>
                <span>故障类型：{{item.class}}</span>
                <span>服务时间：{{item.time2}}</span>
                <span>故障单号：{{item.num}}</span>
              </div>
             
               <button @click="handleapp()">评价</button>
               <button @click="handletask()">任务记录</button>
            <!-- </router-link> -->
          </li>
        </ul>
      </mt-tab-container-item>

      <mt-tab-container-item id="3">
        <ul>
          <li v-for="(item,index) in list" :key="index">
            <!-- <router-link to="/detail"> -->
              <div>
                <img src="##" alt>
                <span>{{item.name}}</span>
                <span>{{item.time}}</span>
              </div>
              <div>
                <span>故障类型：{{item.class}}</span>
                <span>服务时间：{{item.time2}}</span>
                <span>故障单号：{{item.num}}</span>
                <span>取消原因：自己修好了</span>
                <span>取消时间: 2019-05-01</span>
              </div>
            <!-- </router-link> -->
          </li>
        </ul>
      </mt-tab-container-item>
    </mt-tab-container>
    <Footer-com/>
  </div>
</template>

<script>
import Footer from "../common/footer";
export default {
  data() {
    return {
      selected: "1",
      list: [
        {
          path: "",
          img: "",
          name: "李小刚",
          time: "2019-4-15",
          class: "液位仪",
          time2: "2019-4-15",
          num: "210922199312202112"
        },
        {
          path: "",
          img: "",
          name: "李小刚",
          time: "2019-4-15",
          class: "液位仪",
          time2: "2019-4-15",
          num: "210922199312202112"
        }
      ]
    };
  },
  components: {
    "Footer-com": Footer
  },
  methods: {
    handletask() {
      this.$router.push("/task");
    },
     handleapp() {
      this.$router.push("/appraise");
    },
  }
};
</script>


<style scoped>
</style>