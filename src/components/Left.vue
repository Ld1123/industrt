<template>
  <div class="left">
    <div class="left-top">
      <div class="one">
        <h1>空气质量实况</h1>
        <div class="showTime">{{ nowDate }}{{ nowTime }}</div>
         <left-one></left-one>
      </div>
      <i></i>
      <div class="two">
        <ul>
          <li>
            <span class="first">8</span>
            <div class="zi"></div>
            <h5>PM2.5</h5>
          </li>
          <li>
            <span class="second">8</span>
            <div class="huang"></div>
            <h5>PM10</h5>
          </li>
          <li>
            <span class="third">8</span>
            <div class="ju"></div>
            <h5>O3</h5>
          </li>
          <li>
            <span class="fourth">8</span>
            <div class="lv"></div>
            <h5>SO2</h5>
          </li>
          <li>
            <span class="fiveth">8</span>
            <div class="fen"></div>
            <h5>NO2</h5>
          </li>
          <li>
            <span class="sixth">8</span>
            <div class="cheng"></div>
            <h5>CO</h5>
          </li>
        </ul>
      </div>
      <i></i>
      <div class="three">
        <ul>
          <li>
            <div class="you">优</div>
            <span>AOI:54</span>
            <h5>8月20</h5>
          </li>
          <li>
            <div class="liang">良</div>
            <span>AOI:54</span>
            <h5>8月20</h5>
          </li>
          <li>
            <div class="qing">轻度</div>
            <span>AOI:54</span>
            <h5>8月20</h5>
          </li>
          <li>
            <div class="zhong">中度</div>
            <span>AOI:54</span>
            <h5>8月20</h5>
          </li>
          <li>
            <div class="du">重度</div>
            <span>AOI:54</span>
            <h5>8月20</h5>
          </li>
        </ul>
      </div>
      <i class="i">
        <p class="yi"></p>
        <p class="er"></p>
        <p class="san"></p>
        <p class="si"></p>
        <p class="wu"></p>
      </i>
      <div class="four"></div>
    </div>
    <div class="left-bottom"></div>
  </div>
</template>

<script>
import LeftOne from './LeftOne.vue';

export default {
  components: { LeftOne },
  data() {
    return {
      nowDate: "", // 当前日期
      nowTime: "", // 当前时间
      nowWeek: "", // 当前星期
    };
  },
  created() {},
  computed: {},
  methods: {
    dealWithTime(data) {
      // 获取当前时间

      let Y = data.getFullYear();
      let M = data.getMonth() + 1;
      let D = data.getDate();
      let H = data.getHours();
      let Min = data.getMinutes();
      let S = data.getSeconds();
      D = D < 10 ? "0" + D : D;
      M = M < 10 ? "0" + M : M;
      H = H < 10 ? "0" + H : H;
      S = S < 10 ? "0" + S : S;
      Min = Min < 10 ? "0" + Min : Min;
      this.nowDate = Y + "-" + M + "-" + D + " ";

      this.nowTime = H + ":" + Min + ":" + S + " " + "发布";
      // formatDateTime = Y + "年" + M + "月" + D + "日 " + " 周" +W + H + ":" + Min + ":" + S;
    },
  },
  mounted() {
    // 页面加载完后显示当前时间
    this.dealWithTime(new Date());
    // 定时刷新时间
    this.timer = setInterval(() => {
      this.dealWithTime(new Date()); // 修改数据date
    }, 500);
  },
  destroyed() {
    if (this.timer) {
      // 注意在vue实例销毁前，清除我们的定时器
      clearInterval(this.timer);
    }
  },
};
</script>

<style scoped>
.yi{
  content: '';
  width: 10px;
  height: 10px;
  background:  #66CCFFFF;
  border-radius: 50px;
  position: absolute;
  left: 35px;
  bottom: -4px;
}
.er{
  content: '';
  width: 10px;
  height: 10px;
  background:  #66CCFFFF;
  border-radius: 50px;
  position: absolute;
  left: 131px;
  bottom: -4px;
}
.san{
  content: '';
  width: 10px;
  height: 10px;
  background:  #66CCFFFF;
  border-radius: 50px;
  position: absolute;
  left: 226px;
  bottom: -4px;
}
.si{
  content: '';
  width: 10px;
  height: 10px;
  background:  #66CCFFFF;
  border-radius: 50px;
  position: absolute;
  left: 322px;
  bottom: -4px;
}
.wu{
  content: '';
  width: 10px;
  height: 10px;
  background:  #66CCFFFF;
  border-radius: 50px;
  position: absolute;
  left: 417px;
  bottom: -4px;
}
.i{
  display: block;
  content: "";
  width: 461px;
  height: 2px;
  background: #66CCFFFF;
  position: absolute;
  left: 37px;
  
}
i {
  display: block;
  content: "";
  width: 461px;
  height: 1px;
  background: #234badff;
  position: absolute;
  left: 37px;
}
.left {
  height: 754px;
  width: 534px;
}
.left .left-top {
  width: 534px;
  height: 538px;
  background: url(../image/kongqi.png);
  position: relative;
}
.left .left-top .one {
  width: 534px;
  height: 235px;
  position: relative;
}

.left .left-top .one h1 {
  display: inline-block;
  width: 132px;
  height: 33px;
  font-size: 22px;
  font-family: SourceHanSansCN-Bold, SourceHanSansCN;
  font-weight: bold;
  color: #ffffff;
  line-height: 33px;
  position: absolute;
  top: 30px;
  left: 38px;
}
.left .left-top .one .showTime {
  position: absolute;
  top: 30px;
  right: 36px;
  height: 33px;
  font-size: 22px;
  font-family: SourceHanSansCN-Medium, SourceHanSansCN;
  font-weight: 500;
  color: #f7b500;
  line-height: 33px;
}







.left .left-top .two {
  width: 534px;
  height: 125px;
  position: relative;
}
.left .left-top .two ul{
  width: 458px;
  height: 100px;
  display: flex;
  position: absolute;
  left: 47px;
  top: 12px;
}
.left .left-top .two ul li{
  width: 51px;
  height: 100px;
  margin-right: 26px;
}
.left .left-top .two ul li .first{
  display: block;
  width: 9px;
height: 16px;
font-size: 16px;
font-family: SourceHanSansCN-Regular, SourceHanSansCN;
font-weight: 400;
color: #FFFFFF;
line-height: 16px;
margin-left: 22px;
margin-bottom: 1px;
}
.left .left-top .two ul li .second{
  display: block;
  width: 9px;
height: 16px;
font-size: 16px;
font-family: SourceHanSansCN-Regular, SourceHanSansCN;
font-weight: 400;
color: #FFFFFF;
line-height: 16px;
margin-left: 22px;
margin-bottom: 1px;
margin-top: 8px;
}
.left .left-top .two ul li .third{
  display: block;
  width: 9px;
height: 16px;
font-size: 16px;
font-family: SourceHanSansCN-Regular, SourceHanSansCN;
font-weight: 400;
color: #FFFFFF;
line-height: 16px;
margin-left: 22px;
margin-bottom: 1px;
margin-top: 9px;
}
.left .left-top .two ul li .fourth{
  display: block;
  width: 9px;
height: 16px;
font-size: 16px;
font-family: SourceHanSansCN-Regular, SourceHanSansCN;
font-weight: 400;
color: #FFFFFF;
line-height: 16px;
margin-left: 22px;
margin-bottom: 1px;
margin-top: 18px;
}
.left .left-top .two ul li .fiveth{
  display: block;
  width: 9px;
height: 16px;
font-size: 16px;
font-family: SourceHanSansCN-Regular, SourceHanSansCN;
font-weight: 400;
color: #FFFFFF;
line-height: 16px;
margin-left: 22px;
margin-bottom: 1px;
margin-top: 10px;
}
.left .left-top .two ul li .sixth{
  display: block;
  width: 9px;
height: 16px;
font-size: 16px;
font-family: SourceHanSansCN-Regular, SourceHanSansCN;
font-weight: 400;
color: #FFFFFF;
line-height: 16px;
margin-left: 22px;
margin-bottom: 1px;
margin-top: 4px;
}
.left .left-top .two ul li .zi{
  width: 32px;
height: 61px;
background: linear-gradient(180deg, #D882FE 0%, #AA27F5 100%);
margin-left: 10px;
}
.left .left-top .two ul li .huang{
  width: 32px;
height: 53px;
background: linear-gradient(180deg, #F3E683 0%, #E9ED47 100%);
margin-left: 10px;
}
.left .left-top .two ul li .ju{
  width: 32px;
height: 52px;
background: linear-gradient(180deg, #E56E59 0%, #E64F31 100%);
margin-left: 10px;
}
.left .left-top .two ul li .lv{
  width: 32px;
height: 43px;
background: linear-gradient(180deg, #51F7B4 0%, #31DBA1 100%);
margin-left: 10px;
}
.left .left-top .two ul li .fen{
  width: 32px;
height: 52px;
background: linear-gradient(180deg, #EC58AC 0%, #CB2087 100%);
margin-left: 10px;
}
.left .left-top .two ul li .cheng{
  width: 32px;
height: 57px;
background: linear-gradient(180deg, #F29B56 0%, #FE751A 100%);
margin-left: 10px;
}
.left .left-top .two ul li h5{
width: 51px;
height: 18px;
font-size: 18px;
font-family: SourceHanSansCN-Regular, SourceHanSansCN;
font-weight: 400;
color: #FFFFFF;
line-height: 18px;
text-align: center;
margin-top: 4px;
}







.left .left-top .three {
  width: 534px;
  height: 137px;
  position: relative;
}
.left .left-top .three ul {
  display: flex;
  width: 478px;
  height: 116px;
  position: absolute;
  left: 43px;
  top: 16px;
}
.left .left-top .three ul li {
  width: 68px;
  height: 116px;
  margin-right: 28px;
}
.left .left-top .three ul li span {
  display: block;
  width: 55px;
  height: 18px;
  font-size: 18px;
  font-family: SourceHanSansCN-Regular, SourceHanSansCN;
  font-weight: 400;
  color: #ffffff;
  line-height: 27px;
  margin-left: 7px;
}
.left .left-top .three ul li h5 {
  margin-top: 7px;
  margin-left: 13px;
  height: 16px;
  font-size: 16px;
  font-family: SourceHanSansCN-Regular, SourceHanSansCN;
  font-weight: 400;
  color: #66ccff;
  line-height: 24px;
}

.left .left-top .three ul li .you {
  width: 68px;
  height: 68px;
  color: #ffffffff;
  font-size: 20px;
  text-align: center;
  line-height: 68px;
  border-radius: 50px;
  background: linear-gradient(180deg, #1d9599 0%, #125874 100%);
}
.left .left-top .three ul li .liang {
  width: 68px;
  height: 68px;
  color: #ffffffff;
  font-size: 20px;
  text-align: center;
  line-height: 68px;
  border-radius: 50px;
  background: linear-gradient(180deg, #a59c7a 0%, #676d60 100%);
}
.left .left-top .three ul li .qing {
  width: 68px;
  height: 68px;
  color: #ffffffff;
  font-size: 20px;
  text-align: center;
  line-height: 68px;
  border-radius: 50px;
  background: linear-gradient(180deg, #cf969f 0%, #423b67 100%);
}
.left .left-top .three ul li .zhong {
  width: 68px;
  height: 68px;
  color: #ffffffff;
  font-size: 20px;
  text-align: center;
  line-height: 68px;
  border-radius: 50px;
  background: linear-gradient(180deg, #994467 0%, #593a61 100%);
}

.left .left-top .three ul li .du {
  width: 68px;
  height: 68px;
  color: #ffffffff;
  font-size: 20px;
  text-align: center;
  line-height: 68px;
  border-radius: 50px;
  background: linear-gradient(180deg, #902892 0%, #522375 100%);
}

.left .left-bottom {
  width: 534px;
  height: 216px;
  background: url(../image/shujubianhua.png);
}
</style>
