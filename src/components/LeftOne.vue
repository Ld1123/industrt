<template>
    <div class="pollutant">
        <div id="app">
            <div id="mai" style="width: 120px;height: 125px;"></div>
            <span class="san">300</span>
            <span class="AOI">AOI</span>
        </div>
        <div id="app">
            <div id="Main" style="width: 170px;height: 125px;"></div>
            <span class="PM">PM2.5</span>
            <span class="shou">首要污染物</span>
        </div>
        <div class="three">
            <div class="one">
                <span class="yan">严重</span>
                <div class="two">

                </div>
            </div>
            <span class="SHOU">
                首要污染物
            </span>
        </div>
    </div>
</template>

<script>
export default {
  components: {},
  methods: {
    drawChart() {
      // 基于准备好的dom，初始化echarts实例
      let myChart = this.$echarts.init(document.getElementById("mai"));
      // 指定图表的配置项和数据
      let option = {
      series: [{
          center:['60px','70px'],
        type: 'gauge',
        radius:'60',
        progress: {
            show: true,
            width: 11
        },
        axisLine: {
            lineStyle: {
                
                width: 0,
                
            }
        },
        axisTick: {
            show: false,
              
        },
        splitLine: {
            length: 0,
            lineStyle: {
                width: 0,
                
            }
        },
        axisLabel: {
            distance: 0,
            color: 'red',
            fontSize: 0
        },
        anchor: {
            show: false,
            showAbove: false,
            size: 0,
            itemStyle: {
                borderWidth: 0
            }
        },
        pointer: {
                        //这个show属性好像有问题，因为在这次开发中，需要去掉指正，我设置false的时候，还是显示指针，估计是BUG吧，我用的echarts-3.2.3；希望改进。最终，我把width属性设置为0，成功搞定！
                        show: false,
                        //指针长度
                        length:'90%',
                        width:0,
                        
                    },
        title: {
            show: false
        },
       
        detail: {
            valueAnimation: false,
            fontSize: 0,
            offsetCenter: [0, 0]
        },
        data: [{
            value: 100,
            
        }]
    }]
        };

      // 使用刚指定的配置项和数据显示图表。
      myChart.setOption(option);
    },
       drawCharts() {
      // 基于准备好的dom，初始化echarts实例
      let myChart = this.$echarts.init(document.getElementById("Main"));
      // 指定图表的配置项和数据
      let option = {
      series: [{
          center:['105px','70px'],
        type: 'gauge',
        radius:'60',
        progress: {
            show: true,
            width: 11
        },
        axisLine: {
            lineStyle: {
                
                width: 0,
                
            }
        },
        axisTick: {
            show: false,
              
        },
        splitLine: {
            length: 0,
            lineStyle: {
                width: 0,
                
            }
        },
        axisLabel: {
            distance: 0,
            color: 'red',
            fontSize: 0
        },
        anchor: {
            show: false,
            showAbove: false,
            size: 0,
            itemStyle: {
                borderWidth: 0
            }
        },
        pointer: {
                        //这个show属性好像有问题，因为在这次开发中，需要去掉指正，我设置false的时候，还是显示指针，估计是BUG吧，我用的echarts-3.2.3；希望改进。最终，我把width属性设置为0，成功搞定！
                        show: false,
                        //指针长度
                        length:'90%',
                        width:0,
                        
                    },
        title: {
            show: false
        },
       
        detail: {
            valueAnimation: false,
            fontSize: 0,
            offsetCenter: [0, 0]
        },
        data: [{
            value: 100,
            
        }]
    }]
        };

      // 使用刚指定的配置项和数据显示图表。
      myChart.setOption(option);
    },
  },
  mounted() {
    this.drawChart();
    this.drawCharts()
  },
};
</script>

<style scoped>
.pollutant{
    width: 452px;
    height: 143px;
    display: flex;
    position: absolute;
    top: 78px;
    right: 40px;
    
}
.pollutant .three{
    width: 126px;
height: 143px;
background: #02194F;
border: 1px solid #2A56C1;
position: absolute;
top: 0px;
right: 0px;

}
.pollutant .three .one{
    width: 90px;
height: 90px;
border: 1px solid #44D7B6;
border-radius: 50px;
text-align: center;
margin: 13px auto 10px;
}
.pollutant .three .one .two{
   width: 78px;
height: 44px;

background: #44D7B6FF;
position: absolute;
top: 53px;
left: 23px;
border-radius: 10px 10px 70px 70px;
}
.pollutant .three .one .yan{
    width: 40px;
height: 20px;
font-size: 20px;
font-family: SourceHanSansCN-Medium, SourceHanSansCN;
font-weight: 500;
color: #35AD9F;
line-height: 20px;
position: absolute;
top: 28px;
left: 43px;
}
.pollutant .three .SHOU{
    width: 90px;
height: 18px;
font-size: 18px;
font-family: SourceHanSansCN-Regular, SourceHanSansCN;
font-weight: 400;
color: #FFFFFF;
line-height: 18px;
position: absolute;
top: 113px;
left: 17px;
}
#app .san{
    width: 35px;
    height: 20px;
    font-size: 20px;
    font-family: SourceHanSansCN-Medium, SourceHanSansCN;
    font-weight: 500;
    color: #FFFFFF;
    line-height: 30px;
    position: absolute;
    top: 52px;
    left: 44px;
}
#app .AOI{
    width: 30px;
    height: 18px;
    font-size: 18px;
    font-family: SourceHanSansCN-Regular, SourceHanSansCN;
    font-weight: 400;
    color: #FFFFFF;
    line-height: 27px;
    position: absolute;
    top: 113px;
    left: 44px;
}
#app .PM{
    width: 59px;
height: 20px;
font-size: 20px;
font-family: SourceHanSansCN-Medium, SourceHanSansCN;
font-weight: 500;
color: #FFFFFF;
line-height: 30px;

    position: absolute;
    top: 52px;
    left: 198px;
}
#app .shou{
   width: 90px;
height: 18px;
font-size: 18px;
font-family: SourceHanSansCN-Regular, SourceHanSansCN;
font-weight: 400;
color: #FFFFFF;
line-height: 27px;

    position: absolute;
    top: 113px;
    left: 180px;
}
</style>
