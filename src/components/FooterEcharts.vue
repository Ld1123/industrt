<template>
  <div id="app">
    <div id="mains" style="width: 532px; height: 225px"></div>
  </div>
</template>

<script>
export default {
  name: "app",
  methods: {
    drawChart() {
      // 基于准备好的dom，初始化echarts实例
      let myChart = this.$echarts.init(document.getElementById("mains"));
      // 指定图表的配置项和数据
      let option = {
        title: {
          text: "水质监测",
          left: "35px",
          top: "28px",
          textStyle: {
            fontSize: "22px",
            color: "#FFFFFF",
            fontWeight: "600",
          },
        },
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
          top: 70,
          bottom: 50,
          left:35,
          right:35
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
            name: "目标水质",
            type: "line",
            xAxisIndex: 1,
            smooth: true,
            symbol: "circle",
            symbolSize: 0,
            itemStyle: {
              normal: { color: "#66CCFFFF" },
            },
            data: [
              48,
              65,
              1,
              51,
              151,
              30,
              126,
              350,
              15,
              32,
              61,
              51,
              120,
              21,
              52,
              68,
              130,
              160,
              58,
              160,
              32,
              170,
              62,
              12,
              61,
              190,
              65,
              170,
              160,
              65,
              130,
              79,
              160,
              80,
            ],
          },
          {
            name: "当前水质",
            type: "line",
            xAxisIndex: 1,
            smooth: true,
            symbol: "circle",
            symbolSize: 0,
            itemStyle: {
              normal: { color: "#FF4A6AFF" },
            },
            data: [
              200,
              150,
              300,
              130,
              15,
              110,
              62,
              31,
              47,
              49,
              150,
              200,
              165,
              187,
              31,
              1,
              40,
              12,
              31,
              110,
              60,
              75,
              18,
              51,
              74,
              160,
              170,
              200,
              31,
              14,
              115,
              13,
              116,
              160,
            ],
          },
        ],
      };

      // 使用刚指定的配置项和数据显示图表。
      myChart.setOption(option);
    },
  },
  mounted() {
    this.drawChart();
  },
};
</script>
<style scoped>
</style>
