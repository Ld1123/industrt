<template>
  <div class="right-bottom">
    <div class="ones">
      <div class="p">污染源监测</div>
      <right-two></right-two>
    </div>
    <div class="app">
      <div id="mainss" style="width: 461px; height: 119px"></div>
    </div>
  </div>
</template>

<script>
import RightTwo from './RightTwo.vue';
export default {
  components: { RightTwo },
  name: "app",
  created() {},
  computed: {},
  methods: {
    drawChart() {
      let myChart = this.$echarts.init(document.getElementById("mainss"));
      let option = {
        tooltip: {
          trigger: "none",
          axisPointer: {
            type: "shadow",
          },
        },
        legend: {
          data: ["2015 降水量", "2016 降水量"],
        },
        grid: {
          top: 0,
          bottom: 53,
          left: -16,
          right: -16,
        },
        legend: {
          icon: "circle", //  字段控制形状  类型包括 circle，rect,line，roundRect，triangle，diamond，pin，arrow，none
          itemWidth: 10, // 设置宽度
          itemHeight: 10, // 设置高度
          itemGap: 10, // 设置间距

          right: "41px",
          top: "45px",

          textStyle: {
            //图例文字的样式
            color: "#fff",
            fontWeight: "400",
            fontSize: 16,
          },
        },
        xAxis: [
          {
            data: ["8-20", "8-20", "8-20", "8-20", "8-20", "8-20", "8-20"],
            axisLine: {
              lineStyle: {
                color: "#fff",
                
              },
            },
            axisTick: {
              show: false,
            },
          },
          {
            type: "category",
            axisLine: {
              onZero: true,
              lineStyle: {
                color: "#061F5DFF",
                
              },
            },
          },
        ],

        yAxis: [
          {
            axisLine: {
              show: false,
            },
            axisTick: {
              show: false,
            },
            minorTick: {
              show: false,
            },
            splitLine: {
              show: false,
            },
            axisLabel: {
              formatter: function () {
                return "";
              },
            },
            minInterval: 20, //最小值
            interval: 20,
            max: 350, //纵坐标最大值
          },
          {
            splitLine: {
              show: false,
            },
          },
          {
            type: "value",
          },
        ],

        series: [
          {
            lineStyle: {
              color: "#8872FFFF",
              width: 1,
            },
            areaStyle: {
              normal: {
                color: "#8872FFFF", //改变区域颜色
              },
            },
            type: "line",
            xAxisIndex: 1,
            smooth: true,
            symbol: "circle",
            symbolSize: 0,
            itemStyle: {
              normal: { color: "#6236FFFF" },
            },
            data: [240, 300, 200, 150, 300, 220, 280, 180, 300, 180, 300, 200],
          },
        ],
      };
      myChart.setOption(option);
    },
  },
  mounted() {
    this.drawChart();
  },
};
</script>

<style scoped>
.app {
  width: 461px;
  height: 119px;
  position: absolute;
  top: 229px;
  left: 35px;
}
.right .right-bottom {
  width: 532px;
  height: 348px;
  position: relative;
  background: url(../image/wuranyuanjiance.png);
}
.ones {
  width: 461px;
  height: 171px;
  padding: 28px 36px 29px 35px;
}
.ones .p {
  width: 110px;
  height: 22px;
  font-size: 22px;
  margin-left: 1px;
  font-family: SourceHanSansCN-Bold, SourceHanSansCN;
  font-weight: bold;
  color: #ffffff;
  line-height: 33px;
}

</style>
