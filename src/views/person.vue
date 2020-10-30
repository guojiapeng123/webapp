<template>
    <div>
        <header>
            <div class="header">
                <span style="font-size: 25px;color: white"><strong>青木商城</strong></span>
                <span class="title">首页</span>
                <div class="search">
                    <input type="search"/>
                    <button>搜索</button>
                </div>
            </div>
        </header>
        <div class="main">
            <div class="left">
                <div class="head">
                    全部功能
                </div>
                <div class="list">
                    <div v-for="i in wordlist" :key="i">
                        {{i}}
                    </div>
                </div>
            </div>
            <div class="middle">
                <div class="personinformation">
                        <div class="upper">
                            <div class="header">
                                <img :src="require('@/assets/logo.png')"/>
                            </div>
                            <span >我的收货地址</span>
                            <span >我的优惠信息</span>
                            <span >我的支付宝</span>
                        </div>
                        <div class="buttom">
                            <span v-for="item in informationlist" :key="item">{{item}}</span>
                        </div>
                </div>
                <div class="transport">
                    <span class="iconfont icon-tubiaolunkuo-"></span>
                    <span style="margin-left: 5px">我的物流</span>
                </div>
                <div class="recommend">
                    <div class="head">
                        <span>根据浏览，猜我喜欢</span>
                        <button >换一批</button>
                    </div>
                    <div class="inner">
                        <div class="card" v-for="i in 9" :key="i">
                            <img style="height: 220px;background-color: white"  :src="require('@/assets/png11.png')"/>
                            <div class="information">
                                <div>
                                    <span style="color: red">￥50</span>
                                    <del style="font-size: 12px">￥70</del>
                                </div>
                                <div style="font-size: 8px">vue大减价你来不来</div>
                                <div class="sale">月销:2333</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="right">
                <div class="calendar">
                    <div class="head">
                        <span >我的日历</span>
                    </div>
                    <div class="inner">
                        <div style="font-weight: bold;font-size: 30px">{{date.Date}}</div>
                        <div>{{date.day}}</div>
                        <div>{{date.year+" "+date.month}}</div>
                    </div>
                </div>
                <div class="service">
                    <div class="head">便民服务</div>
                    <div class="inner">
                        <div v-for="i in 10" :key="i" :style="cardstyle">
                            <div class=" iconfont icon-tubiaolunkuo-" style="font-size: 18px;color:#a38368">
                            </div>
                            <span style="font-size: 8px;color:#a38368">意思一下</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>

    </div>
</template>

<script>
    export default {
        name: "person",
        data:function () {
            return{
                informationlist:["待付款","待发货","待收货","待评价","退款"],
                date:{
                    year:"2020",
                    month:"10",
                    Date:"29",
                    day:"星期四"
                },
                cardstyle:{
                    border:"solid 1px #a38368",
                    width:"24%"
                },
                wordlist:["我的购物车","已买到的宝贝","我的发票","我的收藏"]
            }
        },

    }
</script>

<style scoped>
    .header{
        width: 100%;
        background-color:#f2f2f0;
        height: 61px;
        display: flex;
        justify-content: space-around;
        align-items: center;
    }
    .header span{
        color: white;
    }
    .icon-taobaowang{
        font-size: 40px;
    }
    .title{
        margin-left: -20%;
    }
    .main{
        height: 800px;
        display: flex;
        justify-content: center;
        width: 100%;
    }
    .middle{
        width: 50%;
        margin-top: 60px;
    }
    .personinformation{
        border: solid 1px rgb(246,241,238);
        height: 144px;
    }
    .personinformation .upper{
        height:50%;
        background-color:#f5f8fa;
        border: solid 1px rgb(246,241,238);
        display: flex;
        justify-content: space-around;
        align-items: center;
    }
    .personinformation .buttom{
        display: flex;
        justify-content: space-around;
        align-items: center;
    }
    .middle .recommend .head{
        margin-top: 50px;
        height: 40px;
        background-color: #a0cdeb;
        display: flex;
        color: white;
        justify-content: space-between;
        align-items: center;
    }
    .middle .recommend .head span{
        margin-left: 10%;
    }
    .middle .recommend .head button{
        margin-right: 5%;
        width: 10%;
        background-color: white;
        border: 0px;
    }
    .personinformation .buttom span{
        height: 20px;
        margin-top:15px;
        padding-right: 20px;
        border-right: solid 3px rgb(245,248,250);
    }
    .personinformation .upper .header{
        width: 200px;
        background-color: #f5f8fa;
    }
    .personinformation .upper .header img{
        height: 60px;
        width: 60px;
        border-radius: 30px;
        background-color: white;
    }
    .personinformation .upper span{
        font-size: 12px;
    }
    .middle .transport{
        margin-top: 50px;
        height: 60px;
        background-color: #f5f8fa;
        display: flex;
        justify-content: flex-start;
        align-items: center;
    }
    .icon-tubiaolunkuo-{
        font-size: 30px;
        margin-left: 10px;
    }
    .middle .recommend .inner{
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;
        background-color: #f5f8fa;

    }
    .middle .recommend .inner .card{
        height: 270px;
        border: solid 1px white;
        margin-top: 10px;
    }
    .middle .recommend .inner .card .information{
        background-color: white;
        height: 50px;
        display: flex;
        flex-direction: column;
    }
    .middle .recommend .inner .card .information .sale{
        display: flex;
        justify-content: flex-end;
        margin-left: 10px;
        font-size: 10px;
        color: #97938e;
    }
    .right{
        display: flex;
        flex-direction: column;
        width: 20%;
        margin-top: 60px;
        margin-left: 20px;
    }
    .right .calendar{
        border: solid 1px #6ec884;
    }
    .right .calendar .head{
        background-color: #6ec884;
        color: white;
        height: 50px;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .right .calendar .inner{
        height: 100px;
        background-color:#b3f0c2 ;
        color: white;
    }
    .right .service{
        margin-top: 20px;
        border: solid 1px rgb(163,131,104);
    }
    .right .service .head{
        background-color: #a38368;
        height: 60px;
        display: flex;
        align-items: center;
        justify-content: center;
        color: white;
    }
    .right .service .inner{
        display: flex;
        flex-wrap: wrap;

    }
    .left{
        margin-top: 60px;
        display: flex;
        justify-content: center;
        width: 20%;
        flex-wrap: wrap;
    }
    .left .head{
        color: #e35219;
        font-size: 20px;
        width: 100%;
        height: 20px;
        margin-bottom: 10px;
    }
    .left .list{
        margin-top: -360px;
        font-size: 15px;
    }
</style>