<template>
  <div>
    <div class="lunbo">
      <img src="../../../static/123.jpg" />
    </div>  
    <div class="showTime">
      <div class="word">欢迎您！下午好！</div>
      <div class="time">{{msg}}</div>
    </div>
    <div class="info">
      <p>Yesterday is history, </p>
      <p>tomorrow is a mystery, </p>
      <p>but today is a gift,</p>
      <p>That is why it is called the present</p>
    </div>
    <i-grid>
      <i-grid-item>
        <i-grid-icon><i-icon type="activity" size="28" color="#80848f" /></i-grid-icon>
        <i-grid-label class="showItem">我的文章</i-grid-label>
      </i-grid-item>
      <i-grid-item>
        <i-grid-icon><i-icon type="document" size="28" color="#80848f"/></i-grid-icon>
        <i-grid-label class="showItem">Vue专栏</i-grid-label>
      </i-grid-item>
      <i-grid-item>
        <i-grid-icon><i-icon type="dynamic" size="28" color="#80848f"/></i-grid-icon>
        <i-grid-label class="showItem">Angular专栏</i-grid-label>
      </i-grid-item>
    </i-grid>
    <i-grid>
      <i-grid-item>
        <i-grid-icon><i-icon type="service" size="28" color="#80848f"/></i-grid-icon>
        <i-grid-label class="showItem">小程序</i-grid-label>
      </i-grid-item>
      <i-grid-item>
        <i-grid-icon><i-icon type="createtask" size="28" color="#80848f"/></i-grid-icon>
        <i-grid-label class="showItem">NodeJS</i-grid-label>
      </i-grid-item>
      <i-grid-item>
        <i-grid-icon><i-icon type="emoji" size="28" color="#80848f"/></i-grid-icon>
        <i-grid-label class="showItem">联系我们</i-grid-label>
      </i-grid-item>
    </i-grid>
  </div>
</template>

<script>
export default {
  data() {
    return {
      msg: "2020-1-8"
    };
  },

  components: {},

  methods: {},

  created() {
    // this.msg = new Date();
    // console.log(this.msg);
  }
};
</script>

<style scoped>
.lunbo {
  height: 220px;
}

.lunbo img{
  width:100%;
}

.showTime{
  display:flex;

}

.word{
  width:250px;
  height:22px;
  margin: 5px;
  padding-top:10px;
  padding-left: 5px;
  color:#5cadff;
  font-size: 14px;
}

.time {
  flex:1;
  height:22px;
  margin: 5px;
  padding-top:10px;
  padding-left: 5px;
  color:#5cadff;
  font-size: 14px;
}

.info{
  width:100%;
  height:130px;
  text-align:center;
  line-height:2;
  font-size:16px;
  border-top:5px solid #e9eaec;
  border-bottom:5px solid #e9eaec;
  margin-bottom:30px;
  color:#5cadff;
}

.showItem{
  color:#e9eaec;
  font-size:20px;
  height:50px;
}


</style>
