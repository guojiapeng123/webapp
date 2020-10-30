<template>
    <div class="page">
        <div class="header">
            <div class="inner">确认订单</div>
        </div>
        <div class="maininner">
            <div class="head" :style="style">
                <span style="font-size: 25px">当前配置</span>
            </div>
            <div class="middle" :style="style">
                <div style="width: 100%;display: flex;justify-content: flex-start">实例名称:联想拯救者</div>
                <div>
                    <span style="margin-right: 150px">实例个数:3-5</span>
                    <span>系列:专业制</span>
                </div>
            </div>
            <div class="footer" :style="style">
                <span>到期时间:<span style="color: orange">2020-9-20</span></span>
            </div>
        </div>
        <div class="change">
            <div class="head">
                配置变换
            </div>
            <div class="column">
                基本配置
            </div>
            <div class="inner">
                <div class="series" :style="style">
                    <span style="margin-right: 50px">系列:</span>
                    <button>专业版</button>
                    <button>白金版</button>
                </div>
                <div class="number" :style="style">
                    <span style="font-size: 14px">应用实例个数</span>
                    <button>1-3</button>
                    <button>3-5</button>
                    <button>5-7</button>
                    <button>7-9</button>
                </div>
            </div>
        </div>
        <div class="footer">
            <div class="money">
                <strong>￥0.0</strong>
            </div>
            <div class="button" >
                <button>去支付</button>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "order",
        data:function () {
            return{
                style:{
                    display:"flex",
                    alignItems:"center",
                    justifyContent:"flex-start",
                    marginLeft:"10px",
                    flexWrap:"wrap"
                }
            }
        }
    }
</script>

<style scoped>
    .page .header{
        display: flex;
        justify-content: flex-start;
        width: 100%;
        border-bottom: solid 1px rgb(241,246,249);
    }
    .page{
        display: flex;
        flex-direction: column;
    }
    .page .header .inner{
        color: #44bee3;
        border-left: solid 5px #44bee3;
        font-size: 30px;
        padding-left: 15px;
    }
    .page .maininner{
        height: 200px;
        background-color: #f1f6f9;
        display: flex;
        flex-direction: column;
    }
    .page .maininner .head{
        width: 100%;
        border-bottom: dotted 2px grey;
        height: 60px;
    }
    .page .maininner .middle{
        width: 100%;;
        border-bottom: dotted 2px grey;
        height: 100px;
    }
    .page .maininner .footer{
        height: 60px;
    }
    .page .change .head{
        width: 100%;
        font-size: 20px;
        display: flex;
        justify-content: flex-start;
        border-bottom: dotted 2px grey;
        padding-bottom: 20px;
    }
    .page .change{
        margin-top: 50px;
    }
    .page .change .column{
        background-color: #f2f2f2;
        width: 260px;
        height: 20px;
        font-size: 12px;
        transform: rotate(-90deg);
        margin-top: 140px;
        margin-left: -100px;
    }
    .page .change .inner{
        background-color: #fafafa;
        height: 260px;
        width: 80%;
        margin-left: 40px;
        margin-top: -140px;
    }
    .page .change .inner  button{
        width: 120px;
        border: solid 1px white;
    }
    .page .change .inner  button:hover{
        background-color:#44bee3 ;
    }
    .page .change .inner .series{
      padding-top: 40px;
    }
    .page .change .inner .number{
        padding-top: 80px;
    }
    .footer{

        flex-wrap: wrap;
    }
    .money{
        display: flex;
        justify-content: flex-end;
    }
    .footer .button{
        margin-top:20px;
        display: flex;
        justify-content: flex-end;
    }
    .footer .button button{
        width: 120px;
        height: 40px;
        color: white;
        background-color: orange;
        border: solid 0px;
    }

</style>