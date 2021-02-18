<template>
  <div class="one">
    <div class="th">
      <tr>
        <td>类型</td>
        <td>监测点</td>
        <td>检测值</td>
        <td>日均值</td>
        <td>峰值</td>
        <td>操作</td>
      </tr>
    </div>
    <div class="two">
      <vue-seamless-scroll :data="listData" :class-option="defaultOption" >
        
          <tr v-for="(item, index) in listData" :key="index" class="td">
            <td class="lx">{{ item.jiance }}</td>
            <td class="jc">{{ item.feishui }}</td>
            <td class="cz">{{ item.feiqi }}</td>
            <td class="rj">{{ item.youyan }}</td>
            <td class="fz">{{ item.vocs }}</td>
            <td class="dw">{{ item.caozuo }}</td>
            
          </tr>
       
      </vue-seamless-scroll>
    </div>
  </div>
</template>
<script>
import vueSeamlessScroll from "vue-seamless-scroll";
export default {
  name: "Example3",
  // import引入的组件需要注入到对象中才能使用
  components: {
    vueSeamlessScroll,
  },
  data() {
    // 这里存放数据
    return {
      listData: [],
    };
  },
  // 监听属性 类似于data概念
  computed: {
    defaultOption() {
      return {
        step: 1, // 数值越大速度滚动越快
        limitMoveNum: 2, // 开始无缝滚动的数据量 this.dataList.length
        hoverStop: true, // 是否开启鼠标悬停stop
        direction: 1, // 0向下 1向上 2向左 3向右
        openWatch: true, // 开启数据实时监控刷新dom
        singleHeight: 0, // 单步运动停止的高度(默认值0是无缝不停止的滚动) direction => 0/1
        singleWidth: 0, // 单步运动停止的宽度(默认值0是无缝不停止的滚动) direction => 2/3
        waitTime: 1000, // 单步运动停止的时间(默认值1000ms)
      };
    },
  },
  // 方法集合
  methods: {},
  // 监控data中的数据变化
  watch: {},
  // 生命周期 - 创建完成（可以访问当前this实例）
  created() {},
  // 生命周期 - 挂载完成（可以访问DOM元素）
  mounted() {
    for (let i = 0; i < 15; i++) {
      let j = {
        jiance: "尾气",
        feishui: "点1",
        feiqi: "200",
        youyan: "200",
        vocs: "200",
        caozuo: "定位",
      };
      this.listData.push(j);
    }
  },
};
</script>
 

<style scoped>
.one{
  width:461px;
  height: 137px;
  margin-left: 0px;
  margin-top: 18px;
}
.one .th{
  margin-bottom: 3px;
  width: 461px;
  height: 32px;
  background: linear-gradient(90deg, #078CFC 0%, #132C76 100%);
}
.one .th td{
  display:inline-block;
  height: 18px;
  font-size: 17px;
  font-family: SourceHanSansCN-Medium, SourceHanSansCN;
  font-weight: 500;
  color: #0EDFF9;
  line-height: 30px;
  margin-left: 28px;
}
.one .two{
  width: 461px;
  height: 102px;
  overflow: hidden;
}
.one .two .lx{
  display: inline-block;

  height: 18px;
  font-size: 18px;
  font-family: SourceHanSansCN-Medium, SourceHanSansCN;
  font-weight: 500;
  color: #FFFFFF;
  line-height: 27px;
  margin-left: 28px;
}
.one .two .jc{
  display: inline-block;

  height: 18px;
  font-size: 18px;
  font-family: SourceHanSansCN-Medium, SourceHanSansCN;
  font-weight: 500;
  color:#E31C12FF;
  line-height: 27px;
  margin-left: 34px;
}
.one .two .cz{
  display: inline-block;
  
  height: 18px;
  font-size: 18px;
  font-family: SourceHanSansCN-Medium, SourceHanSansCN;
  font-weight: 500;
  color: #F7B500FF;
  line-height: 27px;
  margin-left: 43px;
}
.one .two .rj{
  display: inline-block;

  height: 18px;
  font-size: 18px;
  font-family: SourceHanSansCN-Medium, SourceHanSansCN;
  font-weight: 500;
  color: #FFFFFF;
  line-height: 27px;
  margin-left: 40px;
}
.one .two .fz{
  display: inline-block;
  
  height: 18px;
  font-size: 18px;
  font-family: SourceHanSansCN-Medium, SourceHanSansCN;
  font-weight: 500;
  color: #FFFFFF;
  line-height: 27px;
  margin-left: 36px;
}
.one .two .dw{
  display: inline-block;
  
  height: 18px;
  font-size: 18px;
  font-family: SourceHanSansCN-Medium, SourceHanSansCN;
  font-weight: 500;
  color: #FFFFFF;
  line-height: 27px;
  margin-left: 24px;
}





.one .two .td{
  width: 461px;
  height: 32px;
  background: #06296B;
  display: inline-block;
  margin-bottom: 2px;
}

</style>
