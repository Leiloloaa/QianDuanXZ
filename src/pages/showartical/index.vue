<template>
  <div>
    <ul v-for="(item,key) in list" :key="key" @click="goContent(item.aid)">
      <li class="list">{{item.title}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      list: []
    };
  },

  components: {},

  methods: {
    requestData() {
      let that = this;
      let api =
        "http://www.phonegap100.com/appapi.php?a=getPortalList&catid=20&page=1";
      wx.request({
        url: api, //仅为示例，并非真实的接口地址
        data: {
          x: "",
          y: ""
        },
        header: {
          "content-type": "application/json" // 默认值
        },
        success(res) {
          // console.log(res.data);
          // 这一步要注意
          that.list = res.data.result;
        }
      });
    },
    goContent(aid) {
      console.log(aid);

      const url = "../articalcontent/main?aid=" + aid;
      mpvue.navigateTo({ url });
    }
  },

  created() {
    this.requestData();
  }
};
</script>

<style scoped>
.list {
  color: #404040;
  font-size: 16px;
  border-bottom: 1px solid #c5c5c5;
  margin: 5px;
  padding-left: 5px;
  /* 单行文本 溢出打点三件套 */
  /* 不换行 */
  white-space: nowrap;
  /* 超出宽度隐藏 */
  overflow: hidden;
  /* 超出文字打点 */
  text-overflow: ellipsis;
  line-height: 2;
}
</style>
