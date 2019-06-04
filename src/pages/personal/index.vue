<template>
    <div class="contain">
        <img src="../../../static/images/logo.jpg" mode="widthFix" alt="">
        <!-- <div class="shopname">
            尹星的店铺
        </div> -->
       <div class="user">
           <img src="../../../static/images/user.png" alt="">
           <p>尹星</p>
       </div>
       <p class="function" @click="jump(0)">我的课程</p>
       <p class="function" @click="jump(1)">历史观看记录</p>
       <p class="function" @click="jump(2)">我的积分</p>
       <p class="loginOut" @click="logout()">登出</p>
    </div>
</template>

<script>
export default {
    data(){
        return{
            shopname:"",
            username:"",
            logo:"",
        }
    },
    methods:{
        jump( index ){
            var url;
            if( index == 0 ){
                url = "../changepwd/main"
            }else if( index == 1 ){
                url = "../mysell/main"
            }else if ( index == 2 ){
                url = "../myreceive/main"
            }
            wx.navigateTo({
                url
            })
        },
        logout(){
            wx.reLaunch({
                url: '../index/main'
            })
        }
    },
    mounted(){
        this.shopname = wx.getStorageSync('shopname')
        this.username = wx.getStorageSync('username')
        this.logo = wx.getStorageSync('logo')
    }

}
</script>

<style lang="less" scoped>
    .contain{
        width: 100%;
        text-align: center;
        >img{
            width: 145px;
            height: 50px;
            margin: 30px 0 0 0 ;
        }
        .shopname{
            height: 48px;
            margin: 0 auto;
            color: #727071;
            font-size: 28px;
        }
        .user{
            margin-top: 20px;
            img{
                width: 100px;
                height: 100px;
                border-radius: 50%;
            }
            p{
                color: black;
                margin-top: 13px;
            }
        }
        .function{
            width: 167px;
            height: 30px;
            line-height: 30px;
            margin: 15px auto;
            border: 1px solid #656364;
            border-radius: 8px;
            font-size: 16px;
            font-weight: 700;
            color: #727272;
        }
        .loginOut{
            width: 167px;
            height: 30px;
            line-height: 30px;
            margin: 15px auto;
            background: black;
            border-radius: 8px;
            font-size: 16px;
            font-weight: 700;
            color: white;
        }

    }
</style>


