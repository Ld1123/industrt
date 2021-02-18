<template>
  <div class="footer">
    <div class="left">
      <div class="ones">
        <div class="p">污染源监测</div>
        <footer-one></footer-one>
      </div>
      <div class="two">
        <p>企业数据监测</p>
        <div class="box">
          <div class="box1">
            <div class="box3">
              <span class="yi">废水</span>
              <span class="er">报警</span>
              <span class="san">12363</span>
              <span class="si">10</span>
            </div>
            <div class="box4">
              <span class="yi">废水</span>
              <span class="er">报警</span>
              <span class="san">12363</span>
              <span class="si">10</span>
            </div>
          </div>
          <div class="box2">
            <div class="box3">
              <span class="yi">废水</span>
              <span class="er">报警</span>
              <span class="san">12363</span>
              <span class="si">10</span>
            </div>
            <div class="box4">
              <span class="yi">废水</span>
              <span class="er">报警</span>
              <span class="san">12363</span>
              <span class="si">10</span>
            </div>
          </div>
        </div>
      </div>
      <div class="three">
        <p>废水实时数据</p>
        <ul>
          <li class="o">
            <span class="top">8</span>
            <div></div>
            <span class="bottom">08:30</span>
          </li>
          <li class="t">
            <span class="top">8</span>
            <div></div>
            <span class="bottom">08:30</span>
          </li>
          <li class="h">
            <span class="top">8</span>
            <div></div>
            <span class="bottom">08:30</span>
          </li>
          <li class="f">
            <span class="top">8</span>
            <div></div>
            <span class="bottom">08:30</span>
          </li>
          <li class="i">
            <span class="top">8</span>
            <div></div>
            <span class="bottom">08:30</span>
          </li>
          <li class="s">
            <span class="top">8</span>
            <div></div>
            <span class="bottom">08:30</span>
          </li>
        </ul>
      </div>
      <div class="four">
          <div class="box1">
              <div class="box3">
                  <img src="../../../image/1.png" alt="">
              </div>
              <div class="box4">
                  <img src="../../../image/2.png" alt="">
              </div>
          </div>
          <div class="box2">
              <div class="box3">
                  <img src="../../../image/3.png" alt="">
              </div>
              <div class="box4">
                  <img src="../../../image/4.png" alt="">
              </div>
          </div>
      </div>
    </div>
    <div class="right">
<FooterEcharts></FooterEcharts>
    </div>
  </div>
</template>

<script>
import FooterEcharts from '@/components/FooterEcharts'
import FooterOne from '@/components/FooterOne.vue';

export default {
  components:{FooterEcharts,FooterOne},
  computed: {},
  methods: {},
  mounted() {},
};
</script>

<style scoped>
.footer {
  width: 1880px;
  display: flex;
  margin: 0px auto;
}
.footer .left {
  display: flex;
  width: 1346px;
  height: 225px;
  background: url(../../../image/wuranyuanjiance1.png);
}
.footer .left .ones {
  width: 352px;
  height: 171px;
  margin: 26px 14px 28px 37px;
}
.footer .left .ones .p {
  width: 110px;
  height: 22px;
  font-size: 22px;
  margin-left: 1px;
  font-family: SourceHanSansCN-Bold, SourceHanSansCN;
  font-weight: bold;
  color: #ffffff;
  line-height: 33px;
}

.footer .left .two {
  width: 273px;
  height: 171px;
  margin: 26px 14px 28px 0px;
}
.footer .left .two p {
  width: 132px;
  height: 22px;
  font-size: 22px;
  font-family: SourceHanSansCN-Bold, SourceHanSansCN;
  font-weight: bold;
  color: #ffffff;
  line-height: 33px;
}
.footer .left .two .box {
  width: 273px;
  height: 137px;
  background: #06296b;
  margin-top: 12px;
}
.footer .left .two .box .box1 {
  display: flex;
  margin-bottom: 7px;
  height: 65px;
  width: 273px;
}
.footer .left .two .box .box1 .box3 {
  width: 133px;
  height: 65px;
  background: #06296b;
  border: 1px solid #0e83e3;
  margin-right: 7px;
  position: relative;
}
.footer .left .two .box .box1 .box3 .yi {
  width: 36px;
  height: 18px;
  font-size: 18px;
  font-family: SourceHanSansCN-Medium, SourceHanSansCN;
  font-weight: 500;
  color: #0edff9;
  line-height: 27px;
  position: absolute;
  top: 8px;
  left: 10px;
}
.footer .left .two .box .box1 .box3 .er {
  width: 32px;
  height: 16px;
  font-size: 16px;
  font-family: SourceHanSansCN-Medium, SourceHanSansCN;
  font-weight: 500;
  color: #e02020;
  line-height: 24px;
  position: absolute;
  top: 8px;
  right: 10px;
}
.footer .left .two .box .box1 .box3 .san {
  width: 45px;
  height: 16px;
  font-size: 16px;
  font-family: SourceHanSansCN-Regular, SourceHanSansCN;
  font-weight: 400;
  color: #0edff9;
  line-height: 24px;
  position: absolute;
  bottom: 9px;
  left: 28px;
}
.footer .left .two .box .box1 .box3 .si {
  width: 18px;
  height: 16px;
  font-size: 16px;
  font-family: SourceHanSansCN-Regular, SourceHanSansCN;
  font-weight: 400;
  color: #e02020;
  line-height: 24px;
  position: absolute;
  bottom: 9px;
  right: 17px;
}
.footer .left .two .box .box1 .box4 {
  width: 133px;
  height: 65px;
  background: #06296b;
  border: 1px solid #0e83e3;
  position: relative;
}
.footer .left .two .box .box1 .box4 .yi {
  width: 36px;
  height: 18px;
  font-size: 18px;
  font-family: SourceHanSansCN-Medium, SourceHanSansCN;
  font-weight: 500;
  color: #0edff9;
  line-height: 27px;
  position: absolute;
  top: 8px;
  left: 10px;
}
.footer .left .two .box .box1 .box4 .er {
  width: 32px;
  height: 16px;
  font-size: 16px;
  font-family: SourceHanSansCN-Medium, SourceHanSansCN;
  font-weight: 500;
  color: #e02020;
  line-height: 24px;
  position: absolute;
  top: 8px;
  right: 10px;
}
.footer .left .two .box .box1 .box4 .san {
  width: 45px;
  height: 16px;
  font-size: 16px;
  font-family: SourceHanSansCN-Regular, SourceHanSansCN;
  font-weight: 400;
  color: #0edff9;
  line-height: 24px;
  position: absolute;
  bottom: 9px;
  left: 28px;
}
.footer .left .two .box .box1 .box4 .si {
  width: 18px;
  height: 16px;
  font-size: 16px;
  font-family: SourceHanSansCN-Regular, SourceHanSansCN;
  font-weight: 400;
  color: #e02020;
  line-height: 24px;
  position: absolute;
  bottom: 9px;
  right: 17px;
}
.footer .left .two .box .box2 {
  display: flex;
  height: 65px;
  width: 273px;
}
.footer .left .two .box .box2 .box3 {
  width: 133px;
  height: 65px;
  background: #06296b;
  border: 1px solid #0e83e3;
  margin-right: 7px;
  position: relative;
}
.footer .left .two .box .box2 .box3 .yi {
  width: 36px;
  height: 18px;
  font-size: 18px;
  font-family: SourceHanSansCN-Medium, SourceHanSansCN;
  font-weight: 500;
  color: #0edff9;
  line-height: 27px;
  position: absolute;
  top: 8px;
  left: 10px;
}
.footer .left .two .box .box2 .box3 .er {
  width: 32px;
  height: 16px;
  font-size: 16px;
  font-family: SourceHanSansCN-Medium, SourceHanSansCN;
  font-weight: 500;
  color: #e02020;
  line-height: 24px;
  position: absolute;
  top: 8px;
  right: 10px;
}
.footer .left .two .box .box2 .box3 .san {
  width: 45px;
  height: 16px;
  font-size: 16px;
  font-family: SourceHanSansCN-Regular, SourceHanSansCN;
  font-weight: 400;
  color: #0edff9;
  line-height: 24px;
  position: absolute;
  bottom: 9px;
  left: 28px;
}
.footer .left .two .box .box2 .box3 .si {
  width: 18px;
  height: 16px;
  font-size: 16px;
  font-family: SourceHanSansCN-Regular, SourceHanSansCN;
  font-weight: 400;
  color: #e02020;
  line-height: 24px;
  position: absolute;
  bottom: 9px;
  right: 17px;
}
.footer .left .two .box .box2 .box4 {
  width: 133px;
  height: 65px;
  background: #06296b;
  border: 1px solid #0e83e3;
  position: relative;
}
.footer .left .two .box .box2 .box4 .yi {
  width: 36px;
  height: 18px;
  font-size: 18px;
  font-family: SourceHanSansCN-Medium, SourceHanSansCN;
  font-weight: 500;
  color: #0edff9;
  line-height: 27px;
  position: absolute;
  top: 8px;
  left: 10px;
}
.footer .left .two .box .box2 .box4 .er {
  width: 32px;
  height: 16px;
  font-size: 16px;
  font-family: SourceHanSansCN-Medium, SourceHanSansCN;
  font-weight: 500;
  color: #e02020;
  line-height: 24px;
  position: absolute;
  top: 8px;
  right: 10px;
}
.footer .left .two .box .box2 .box4 .san {
  width: 45px;
  height: 16px;
  font-size: 16px;
  font-family: SourceHanSansCN-Regular, SourceHanSansCN;
  font-weight: 400;
  color: #0edff9;
  line-height: 24px;
  position: absolute;
  bottom: 9px;
  left: 28px;
}
.footer .left .two .box .box2 .box4 .si {
  width: 18px;
  height: 16px;
  font-size: 16px;
  font-family: SourceHanSansCN-Regular, SourceHanSansCN;
  font-weight: 400;
  color: #e02020;
  line-height: 24px;
  position: absolute;
  bottom: 9px;
  right: 17px;
}

.footer .left .three {
  width: 276px;
  height: 137px;
  background: #06296b;
  margin: 60px 14px 17px 0px;
}
.footer .left .three p {
  display: block;
  width: 108px;
  height: 18px;
  font-size: 18px;
  font-family: SourceHanSansCN-Medium, SourceHanSansCN;
  font-weight: 500;
  color: #0edff9;
  line-height: 27px;
  margin: 8px 84px 10px 84px;
}
.footer .left .three ul {
  display: flex;
}
.footer .left .three ul .o {
  width: 35px;
  height: 92px;
  text-align: center;
  margin-left: 8px;
}
.footer .left .three ul .o .top {
  width: 9px;
  height: 16px;
  font-size: 16px;
  font-family: SourceHanSansCN-Regular, SourceHanSansCN;
  font-weight: 400;
  color: #ffffff;
  line-height: 24px;
}
.footer .left .three ul .o div {
  width: 16px;
  height: 48px;
  background: linear-gradient(180deg, #d882fe 0%, #aa27f5 100%);
  margin: 0px auto;
}
.footer .left .three ul .o .bottom {
  width: 35px;
  height: 14px;
  font-size: 14px;
  font-family: SourceHanSansCN-Regular, SourceHanSansCN;
  font-weight: 400;
  color: #0edff9;
  line-height: 21px;
  display: block;
  margin-top: 6px;
}
.footer .left .three ul .t {
  width: 35px;
  height: 92px;
  text-align: center;
  margin-left: 10px;
}
.footer .left .three ul .t .top {
  width: 9px;
  height: 16px;
  font-size: 16px;
  font-family: SourceHanSansCN-Regular, SourceHanSansCN;
  font-weight: 400;
  color: #ffffff;
  line-height: 24px;
}
.footer .left .three ul .t div {
  width: 16px;
  height: 42px;
  background: linear-gradient(180deg, #f6ea8e 0%, #e6de41 100%);

  margin: 6px auto;
}
.footer .left .three ul .t .bottom {
  width: 35px;
  height: 14px;
  font-size: 14px;
  font-family: SourceHanSansCN-Regular, SourceHanSansCN;
  font-weight: 400;
  color: #0edff9;
  line-height: 21px;
  display: block;
  margin-top: 6px;
}
.footer .left .three ul .h {
  width: 35px;
  height: 92px;
  text-align: center;
  margin-left: 10px;
}
.footer .left .three ul .h .top {
  width: 9px;
  height: 16px;
  font-size: 16px;
  font-family: SourceHanSansCN-Regular, SourceHanSansCN;
  font-weight: 400;
  color: #ffffff;
  line-height: 24px;
}
.footer .left .three ul .h div {
  width: 16px;
  height: 37px;
  background: linear-gradient(180deg, #ec7760 0%, #df4723 100%);

  margin: 11px auto 0px;
}
.footer .left .three ul .h .bottom {
  width: 35px;
  height: 14px;
  font-size: 14px;
  font-family: SourceHanSansCN-Regular, SourceHanSansCN;
  font-weight: 400;
  color: #0edff9;
  line-height: 21px;
  display: block;
  margin-top: 6px;
}
.footer .left .three ul .f {
  width: 35px;
  height: 92px;
  text-align: center;
  margin-left: 10px;
}
.footer .left .three ul .f .top {
  width: 9px;
  height: 16px;
  font-size: 16px;
  font-family: SourceHanSansCN-Regular, SourceHanSansCN;
  font-weight: 400;
  color: #ffffff;
  line-height: 24px;
}
.footer .left .three ul .f div {
  width: 16px;
  height: 37px;
  background: linear-gradient(180deg, #54f7b7 0%, #28e2a6 100%);

  margin: 11px auto 0px;
}
.footer .left .three ul .f .bottom {
  width: 35px;
  height: 14px;
  font-size: 14px;
  font-family: SourceHanSansCN-Regular, SourceHanSansCN;
  font-weight: 400;
  color: #0edff9;
  line-height: 21px;
  display: block;
  margin-top: 6px;
}
.footer .left .three ul .i {
  width: 35px;
  height: 92px;
  text-align: center;
  margin-left: 10px;
}
.footer .left .three ul .i .top {
  width: 9px;
  height: 16px;
  font-size: 16px;
  font-family: SourceHanSansCN-Regular, SourceHanSansCN;
  font-weight: 400;
  color: #ffffff;
  line-height: 24px;
}
.footer .left .three ul .i div {
  width: 16px;
  height: 42px;
  background: linear-gradient(180deg, #f460b0 0%, #d81a86 100%);

  margin: 6px auto;
}
.footer .left .three ul .i .bottom {
  width: 35px;
  height: 14px;
  font-size: 14px;
  font-family: SourceHanSansCN-Regular, SourceHanSansCN;
  font-weight: 400;
  color: #0edff9;
  line-height: 21px;
  display: block;
  margin-top: 6px;
}
.footer .left .three ul .s {
  width: 35px;
  height: 92px;
  text-align: center;
  margin-left: 10px;
}
.footer .left .three ul .s .top {
  width: 9px;
  height: 16px;
  font-size: 16px;
  font-family: SourceHanSansCN-Regular, SourceHanSansCN;
  font-weight: 400;
  color: #ffffff;
  line-height: 24px;
}
.footer .left .three ul .s div {
  width: 16px;
  height: 48px;
  background: linear-gradient(180deg, #f69c66 0%, #f26f1d 100%);

  margin: 0px auto;
}
.footer .left .three ul .s .bottom {
  width: 35px;
  height: 14px;
  font-size: 14px;
  font-family: SourceHanSansCN-Regular, SourceHanSansCN;
  font-weight: 400;
  color: #0edff9;
  line-height: 21px;
  display: block;
  margin-top: 6px;
}

.footer .left .four {
  width: 329px;
  height: 135px;
  margin: 60px 14px 17px 0px;
}
.footer .left .four .box1{
    width: 329px;
    height: 64px;
    display: flex;
}
.footer .left .four .box1 .box3 img{
   
    margin-right: 7px;
    width: 159px;
height: 62px;
background: #D8D8D8;
border: 1px solid #0C71CB;
}
.footer .left .four .box1 .box4 img{
    width: 159px;
height: 62px;
background: #D8D8D8;
border: 1px solid #0C71CB;
}
.footer .left .four .box2{
    width: 329px;
    height: 64px;
    display: flex;
    margin-top: 7px;
}
.footer .left .four .box2 .box3 img{
   
    margin-right: 7px;
    width: 159px;
height: 62px;
background: #D8D8D8;
border: 1px solid #0C71CB;
}
.footer .left .four .box2 .box4 img{
    width: 159px;
height: 62px;
background: #D8D8D8;
border: 1px solid #0C71CB;
}










.footer .right {
  width: 532px;
  height: 225px;
  background: url(../../../image/shuizhijiance.png);
}
</style>
