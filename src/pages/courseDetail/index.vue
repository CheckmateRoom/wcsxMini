<template>
    <div class="contain">
        <img src="../../../static/images/background.jpg" alt="">
        <div class="price">
            <p class="title">手把手教你超火的肠粉做法</p>
            <p class="info">人气273/1课时</p>
        </div>
        <div class="cdy">
            <div class="left">
                <img src="../../../static/images/logo.jpg" alt="">
                <span>稳创食选</span>
            </div>
            <div class="right">
                <button open-type='contact' class="button1">联系客服</button>
            </div>
        </div>
        <div class="courseInfo">
            <p class="info">课程介绍</p>
            <p>阿斯达是阿斯达是阿斯达是阿斯达是阿斯达是阿斯达是阿斯达是阿斯达是阿斯达是阿斯达是阿斯达是阿斯达是阿斯达是阿斯达是阿斯达是阿斯达是阿斯达是阿斯达是阿斯达是阿斯达是阿斯达是阿斯达是阿斯达是阿斯达是</p>
            <p class="info2">视频预览</p>
            <video id="myVideo" src="http://video.jiguiquan.top/63e3071d0e474c84ade475ac22567309/1d6aace3237140e69ce69e332690821e-16b356c8b09e2663af89d4d7bd5d0efb-ld.mp4"  enable-danmu danmu-btn controls></video>
        </div>
        <div class="bottom">
            <div class="discount">
                <p><span>¥8.8或88积分</span><span>¥18.8或168积分</span></p>  
                <p>已有776人购买</p>  
            </div>
            <div class="buy">
                立即购买
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data(){
        return{
            
        }
    },
    methods:{
        
    },
    mounted(){
        
    }

}
</script>

<style lang="less" scoped>
    .contain{
        font-size: 14px;
        >img{
            width: 100%;
            height: 206px;
        }
        .price{
            padding: 15px;
            border-bottom: 2px solid #ededed;
            .title{
                margin-bottom: 13px;
                font-size: 16px;
                font-weight: 700;
            }
            .info{
                color: #b4b4b4;
            }
        }
        .cdy{
            padding: 15px;
            display: flex;
            justify-content: space-between;
            flex-wrap: nowrap;
            border-bottom:  11px solid #eeeeee;
            .left{
                img{
                    width: 30px;
                    height: 30px;
                    border-radius:15px;
                    margin-right: 18px;
                    position: relative;
                    top:4px;
                }
                span{
                    position: relative;
                    top:-4px;
                    font-size: 16px;
                    font-weight: 600;
                }
            }
            .right{
                border: 1px solid #ebd3d2;
                padding: 8px;
                border-radius:3px;
                color: #e76762;
            }
        }
        .courseInfo{
            padding: 17px;
            .info{
                font-size: 16px;
                font-weight: 700;
                padding-bottom: 12px;
                border-bottom:1px solid #ededed;
                margin-bottom: 12px;
            }
            .info2{
                margin-top: 17px;
                font-size: 16px;
                font-weight: 700;
                padding-bottom: 12px;
                border-bottom:1px solid #ededed;
                margin-bottom: 12px;

            }
        }
        .bottom{
            display: flex;
            justify-content: flex-start;
            flex-wrap: nowrap;
            height: 55px;
            border-top: 1px solid #cccccc;
            position: fixed;
            bottom:0;
            .discount{
                width: 262px;
                padding: 5px;
                background-color:white;
                p:first-child{
                    span:first-child{
                        color:#df6b67;
                        font-size: 20px;
                        font-weight: 500;
                        margin-right:15px;
                    }
                    span:last-child{
                        color:#9c9c9c;
                        text-decoration:line-through;
                        position: relative;
                        top: -2px;
                    }
                }
                p:last-child{
                    color:#9c9c9c;
                }
            }
            .buy{
                width: 102px;
                text-align: center;
                line-height: 55px;
                font-size: 16px;
                color: white;
                font-weight: 700;
                background-color: #3c84de;
            }
        }
    }
    
    button{
        background-color:rgb(247, 247, 247); 
        border-radius: 0rpx;
        padding:0rpx;
        margin:0rpx;
        display: inline-block;
        line-height: 1;
        font-size: 14px;
        color:#e76762;
    }

    button::after{ /*button的边框样式是通过::after方式实现的*/
        border:none;
    }

    .button-hover{ /*点击后样式*/
        color:#ebd3d2;
        background-color: rgb(247, 247, 247);
    }
    video{
        width: 100%;
        margin-bottom: 55px;
    }

</style>


