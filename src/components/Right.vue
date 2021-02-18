<template>
  <div class="right">
    <div class="right-top">
      <div id="app">
        <div id="main" style="width: 532px; height: 400px"></div>
      </div>
    </div>
    <right-bottom></right-bottom>
    
  </div>
</template>

<script>
import RightBottom from './RightBottom.vue';
export default {
  components: { RightBottom },
  name: "app",
  methods: {
  




    drawChart() {
      // 基于准备好的dom，初始化echarts实例
      let myChart = this.$echarts.init(document.getElementById("main"));
      // 指定图表的配置项和数据
      let option = {
        title: {
          text: "超标次数分析",
          left: "35px",
          top: "28px",
          textStyle: {
            fontSize: "22px",
            color: "#FFFFFF",
            fontWeight: "600",
          },
        },

        tooltip: {
          trigger: "item",
        },
        legend: {
          icon: "circle", //  字段控制形状  类型包括 circle，rect,line，roundRect，triangle，diamond，pin，arrow，none
          itemWidth: 10, // 设置宽度
          itemHeight: 10, // 设置高度
          itemGap: 10, // 设置间距
          orient: "vertical",
          left: "35px",
          top: "124px",

          textStyle: {
            //图例文字的样式
            color: "#fff",
            fontWeight:'400',
            fontSize: 16,
          },
        },
        series: [
          {
            name: "",
            type: "pie",
            radius: ["50%", "70%"],
            center: ["320px", "220px"],

            avoidLabelOverlap: true,
            itemStyle: {
              borderRadius: 0,
              borderColor: "#fff",
              borderWidth: 1,
            },
            label: {
              show: true,
              position: "bottom",
              textStyle: {
                color: "#FFFFFFFF",
                fontSize: 14,
                fontWeight: "bolder",
              },
            },
            emphasis: {
              label: {
                show: true,
                fontSize: "15",
                fontWeight: "normal",
              },
            },
            labelLine: {
              show: false,
            },
            data: [
              {
                value: 40,
                name: "废水",
                itemStyle: { normal: { color: "#5B8FF9D9" } },
              },
              {
                value: 12,
                name: "废气",
                itemStyle: { normal: { color: "#5AD8A6D9" } },
              },
              {
                value: 12,
                name: "油烟",
                itemStyle: { normal: { color: "#9270CAD9" } },
              },
              {
                value: 12,
                name: "VOCS",
                itemStyle: { normal: { color: "#F6BD16D9" } },
              },
              {
                value: 12,
                name: "尾气",
                itemStyle: { normal: { color: "#E8684AD9" } },
              },
              {
                value: 12,
                name: "噪声",
                itemStyle: { normal: { color: "#6DC8ECD9" } },
              },
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
.right {
  height: 754px;
  width: 534px;
}
.right .right-top {
  width: 532px;
  height: 402px;
  margin-top: 3px;
  background: url(../image/chaobiaochishu.png);
}

</style>
