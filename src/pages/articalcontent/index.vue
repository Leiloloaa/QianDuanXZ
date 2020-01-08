<template>
  <div class="contain">
    <h3 class="title">{{list.title}}</h3>
    <div class="content">
      <wxParse :content="list.content" />
    </div>
  </div>
</template>

<script>
import wxParse from "mpvue-wxparse";

export default {
  data() {
    return {
      list: []
    };
  },

  methods: {
    requestData(aid) {
      let that = this;
      let api =
        "http://www.phonegap100.com/appapi.php?a=getPortalArticle&aid=" + aid;
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
          // 因为只有一个数据 所以说是数组中的第一个对象
          that.list = res.data.result[0];
        }
      });
    }
  },

  onLoad: function(options) {
    // 页面创建时执行
    // 这个 options 就是传过来的值
    let aid = options.aid;
    this.requestData(aid);
  },

  components: {
    wxParse
  }
};
</script>

<style scoped>
@import url("~mpvue-wxparse/src/wxParse.css");

.title {
  font-size: 16px;
  color: red;
  text-align: center;
  width: 100%;
  padding-left: 5px;
  padding-right: 5px;
}
.content {
  padding-left: 5px;
  padding-right: 5px;
  line-height: 2;
}
.content img {
  width: 100%;
}
</style>
