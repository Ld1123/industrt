<template>
     <div class="middle">
        <div class="middle-top">
            <p>监测数据</p>
            <span>图表</span>
            <div class="yi">
                <span>12385</span>
               <div class="fei">废水排放<a>/吨</a></div>
               <div class="tong">同比<a>1234 ↑</a></div>
            </div>
            <div class="y"></div>
            <div class="er">
                <span>12385</span>
               <div class="fei">废气排放<a>/吨</a></div>
               <div class="tong">同比<a>1234 ↑</a></div>
            </div>
            <div class="e"></div>
            <div class="san">
                <span>12385</span>
               <div class="fei">油烟排放<a>/吨</a></div>
               <div class="tong">同比<a>1234 ↑</a></div>
            </div>
            <div class="s"></div>
            <div class="si">
                <span>12385</span>
               <div class="fei">VOCS<a>/吨</a></div>
               <div class="tong">同比<a>1234 ↑</a></div>
            </div>
            <div class="i"></div>
            <div class="wu">
                <span>12385</span>
               <div class="fei">固废转移<a>/吨</a></div>
               <div class="tong">同比<a>1234 ↑</a></div>
            </div>
            
            

        </div>
        <div class="middle-bottom">
            <div class="picture"><img src="../image/ditu.png" alt=""></div>
        </div>
    </div>
</template>

<script>
export default {
   data() {
      return {
      }
   },
   created(){
   },
   computed:{
   },
   methods:{
   },
}
</script>

<style scoped>
.picture{
    padding: 14px 133px 18px 140px;
}
.middle {
  height: 754px;
  width: 812px;
}
.middle .middle-top{
    width: 812px;
    height: 135px;
    margin-top: 5px;
    background: url(../image/jianceshuju.png);
    position: relative;
}
.middle .middle-top .y{
    content: '';
    height: 107px;
    background: #66CCFFFF;
    position: absolute;
    top: 12px;
    left: 200px;
    border: 1px dotted;
}
.middle .middle-top .yi{
    width: 106px;
    height: 94px;
    position: absolute;
    top: 19px;
    left: 79px;
    
}

.middle .middle-top .yi span{
    width: 63px;
height: 22px;
font-size: 22px;
font-family: SourceHanSansCN-Medium, SourceHanSansCN;
font-weight: 500;
color: #66CCFF;
line-height: 33px;
position: absolute;
top: 0;
left: 22px;
}
.middle .middle-top .yi .fei{
width: 106px;
height: 20px;
font-size: 19px;
font-family: SourceHanSansCN-Medium, SourceHanSansCN;
font-weight: 500;
color: #FFFFFF;
line-height: 30px;
position: absolute;
left: 0;
top: 32px;
}
.middle .middle-top .yi .fei a{
    color: #66CCFFFF;
    font-family: SourceHanSansCN-Medium, SourceHanSansCN;
font-weight: 500;
    font-size: 19px;
}
.middle .middle-top .yi .tong{
    width: 80px;
height: 18px;
font-size: 16px;
font-family: SourceHanSansCN-Regular, SourceHanSansCN;
font-weight: 400;
color: #66CCFF;
line-height: 24px;
position: absolute;
bottom: 0;
left: 13px;
}
.middle .middle-top .yi .tong a{
    margin-left: 4px;
    font-size: 14px;
    color: red;
    padding-top: 10px;
}
.middle .middle-top .e{
    content: '';
    height: 107px;
    background: #66CCFFFF;
    position: absolute;
    top: 12px;
    left: 335px;
    border: 1px dotted;
}
.middle .middle-top .er{
    width: 106px;
    height: 94px;
    position: absolute;
    top: 19px;
    left: 216px;
    
}

.middle .middle-top .er span{
    width: 63px;
height: 22px;
font-size: 22px;
font-family: SourceHanSansCN-Medium, SourceHanSansCN;
font-weight: 500;
color: #66CCFF;
line-height: 33px;
position: absolute;
top: 0;
left: 22px;
}
.middle .middle-top .er .fei{
width: 106px;
height: 20px;
font-size: 19px;
font-family: SourceHanSansCN-Medium, SourceHanSansCN;
font-weight: 500;
color: #FFFFFF;
line-height: 30px;
position: absolute;
left: 0;
top: 32px;
}
.middle .middle-top .er .fei a{
    color: #66CCFFFF;
    font-family: SourceHanSansCN-Medium, SourceHanSansCN;
font-weight: 500;
    font-size: 19px;
}
.middle .middle-top .er .tong{
    width: 80px;
height: 18px;
font-size: 16px;
font-family: SourceHanSansCN-Regular, SourceHanSansCN;
font-weight: 400;
color: #66CCFF;
line-height: 24px;
position: absolute;
bottom: 0;
left: 13px;
}
.middle .middle-top .er .tong a{
    margin-left: 4px;
    font-size: 14px;
    color: red;
    padding-top: 10px;
}
.middle .middle-top .s{
    content: '';
    height: 107px;
    background: #66CCFFFF;
    position: absolute;
    top: 12px;
    left: 471px;
    border: 1px dotted;
}
.middle .middle-top .san{
    width: 106px;
    height: 94px;
    position: absolute;
    top: 19px;
    left: 353px;
    
}

.middle .middle-top .san span{
    width: 63px;
height: 22px;
font-size: 22px;
font-family: SourceHanSansCN-Medium, SourceHanSansCN;
font-weight: 500;
color: #66CCFF;
line-height: 33px;
position: absolute;
top: 0;
left: 22px;
}
.middle .middle-top .san .fei{
width: 106px;
height: 20px;
font-size: 19px;
font-family: SourceHanSansCN-Medium, SourceHanSansCN;
font-weight: 500;
color: #FFFFFF;
line-height: 30px;
position: absolute;
left: 0;
top: 32px;
}
.middle .middle-top .san .fei a{
    color: #66CCFFFF;
    font-family: SourceHanSansCN-Medium, SourceHanSansCN;
font-weight: 500;
    font-size: 19px;
}
.middle .middle-top .san .tong{
    width: 80px;
height: 18px;
font-size: 16px;
font-family: SourceHanSansCN-Regular, SourceHanSansCN;
font-weight: 400;
color: #66CCFF;
line-height: 24px;
position: absolute;
bottom: 0;
left: 13px;
}
.middle .middle-top .san .tong a{
    margin-left: 4px;
    font-size: 14px;
    color: red;
    padding-top: 10px;
}
.middle .middle-top .i{
    content: '';
    height: 107px;
    background: #66CCFFFF;
    position: absolute;
    top: 12px;
    left: 606px;
    border: 1px dotted;
}
.middle .middle-top .si{
    width: 106px;
    height: 94px;
    position: absolute;
    top: 19px;
    left: 490px;
    
}

.middle .middle-top .si span{
    width: 63px;
height: 22px;
font-size: 22px;
font-family: SourceHanSansCN-Medium, SourceHanSansCN;
font-weight: 500;
color: #66CCFF;
line-height: 33px;
position: absolute;
top: 0;
left: 22px;
}
.middle .middle-top .si .fei{
width: 80px;
height: 20px;
font-size: 19px;
font-family: SourceHanSansCN-Medium, SourceHanSansCN;
font-weight: 500;
color: #FFFFFF;
line-height: 30px;
position: absolute;
left: 14px;
top: 32px;
}
.middle .middle-top .si .fei a{
    color: #66CCFFFF;
    font-family: SourceHanSansCN-Medium, SourceHanSansCN;
font-weight: 500;
    font-size: 19px;
}
.middle .middle-top .si .tong{
    width: 80px;
height: 18px;
font-size: 16px;
font-family: SourceHanSansCN-Regular, SourceHanSansCN;
font-weight: 400;
color: #66CCFF;
line-height: 24px;
position: absolute;
bottom: 0;
left: 13px;
}
.middle .middle-top .si .tong a{
    margin-left: 4px;
    font-size: 14px;
    color: red;
    padding-top: 10px;
}
.middle .middle-top .wu{
    width: 106px;
    height: 94px;
    position: absolute;
    top: 19px;
    left: 630px;
    
}

.middle .middle-top .wu span{
    width: 63px;
height: 22px;
font-size: 22px;
font-family: SourceHanSansCN-Medium, SourceHanSansCN;
font-weight: 500;
color: #66CCFF;
line-height: 33px;
position: absolute;
top: 0;
left: 22px;
}
.middle .middle-top .wu .fei{
width: 106px;
height: 20px;
font-size: 19px;
font-family: SourceHanSansCN-Medium, SourceHanSansCN;
font-weight: 500;
color: #FFFFFF;
line-height: 30px;
position: absolute;
left: 0;
top: 32px;
}
.middle .middle-top .wu .fei a{
    color: #66CCFFFF;
    font-family: SourceHanSansCN-Medium, SourceHanSansCN;
font-weight: 500;
    font-size: 19px;
}
.middle .middle-top .wu .tong{
    width: 80px;
height: 18px;
font-size: 16px;
font-family: SourceHanSansCN-Regular, SourceHanSansCN;
font-weight: 400;
color: #66CCFF;
line-height: 24px;
position: absolute;
bottom: 0;
left: 13px;
}
.middle .middle-top .wu .tong a{
    margin-left: 4px;
    font-size: 14px;
    color: red;
    padding-top: 10px;
}













.middle .middle-top p{
    width: 20px;
height: 96px;
font-size: 20px;
font-family: SourceHanSansCN-Bold, SourceHanSansCN;
font-weight: bold;
color: #FFFFFF;
line-height: 24px;
position: absolute;
top: 17px;
left: 27px;
}
.middle .middle-top span{
    width: 20px;
height: 48px;
font-size: 20px;
font-family: SourceHanSansCN-Bold, SourceHanSansCN;
font-weight: bold;
color: #66CCFF;
line-height: 24px;
position: absolute;
top: 40px;
right: 28px;
}
.middle .middle-bottom{
    width: 812px;
    height: 611px;
    margin-top: 2px;
    background: url(../image/zhongjian.png);
}
</style>
