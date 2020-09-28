<template>
    <div class="content">
        <section class="profile">
            <HeaderTop title="我的"></HeaderTop>
            <section class="profile-number" @click = "goTo('/login')">
                <a href="javascript:" class="profile-link">
                    <div class="profile_image">
                        <i class="iconfont  icongeren" style="color: white; font-size: 62px "></i>
                    </div>
                    <div class="user-info">
                        <p class="user-info-top">登录/注册</p>
                        <p style="width:127px ; height: 30px; display: flex; justify-content: space-between;align-items: center; margin-left: -7px;">
                            <i class="iconfont iconphone" style="  color: white; font-size: 28px;"></i>
                            <span class="icon-mobile-number" >暂无绑定手机号</span>
                        </p>
                    </div>
                    <span class="arrow">
                        <i class="iconfont iconjiantou1" style="font-size: 12px;"></i>
                    </span>
                </a>
            </section>
            <section class="profile_info_data border-1px">
                <ul class="info_data_list">
                    <a href="javascript:" class="info_data_link">
                        <span class="info_data_top"><span>0.00 </span> 元</span>
                        <span class="info_data_bottom">我的余额</span>
                    </a>
                    <a href="javascript:" class="info_data_link">
                        <span class="info_data_top"><span>0</span> 个</span>
                        <span class="info_data_bottom">我的优惠</span>
                    </a>
                    <a href="javascript:" class="info_data_link">
                        <span class="info_data_top"><span>0</span> 分</span>
                        <span class="info_data_bottom">我的积分</span>
                    </a>
                </ul>
            </section>
            <section class="profile_my_order border-1px">
                <!-- 我的订单 -->
                <a href='javascript:' class="my_order">
                    <span>
                        <i class="iconfont icondingdan" style="font-size: 16px; color: #03556D;"></i>
                    </span>
                    <div class="my_order_div">
                        <span>我的订单</span>
                        <span class="my_order_icon">
                            <i class="iconfont iconjiantou1"></i>
                        </span>
                    </div>
                </a>
                <!-- 积分商城 -->
                <a href='javascript:' class="my_order">
                    <span>
                        <i class="iconfont iconjifen" style="font-size: 18px; color: tomato;"></i>
                    </span>
                    <div class="my_order_div">
                        <span>积分商城</span>
                        <span class="my_order_icon">
                            <i class="iconfont iconjiantou1"></i>
                        </span>
                    </div>
                </a>
                <!-- 华师外卖会员卡 -->
                <a href="javascript:" class="my_order">
                    <span>
                        <i class="iconfont iconhuangguan-VIP" style="color: #FFE4B3; font-size: 18px;"></i>
                    </span>
                    <div class="my_order_div">
                        <span>华师外卖会员卡</span>
                        <span class="my_order_icon">
                            <i class="iconfont iconjiantou1"></i>
                        </span>
                    </div>
                </a>
            </section>
            <section class="profile_my_order border-1px">
                <!-- 服务中心 -->
                <a href="javascript:" class="my_order">
                    <span>
                        <i class="iconfont iconfuwuzhongxin" style="font-size: 18px;  color: #03556D;"></i>
                    </span>
                    <div class="my_order_div">
                        <span>服务中心</span>
                        <span class="my_order_icon">
                            <i class="iconfont iconjiantou1"></i>
                        </span>
                    </div>
                </a>
            </section>
        </section>
    </div>
</template>

<script>
    import HeaderTop from '../../components/HeaderTop/HeaderTop.vue'
    export default {
        components: {
            HeaderTop
        },
        methods: {
            goTo(path){
                this.$router.push(path)
            }
        },
    }
</script>

<style>

    .content>section.profile {
        width: 100%;
        overflow: hidden;
    }
    .content>section.profile .header{
        width: 100%;
        height: 45px;
        background-color: #03556D;
        text-align: center;
        line-height: 45px;
    }
    .content>section.profile .profile-number {
        margin-top: 46px;
    }

    .content>section.profile .profile-number .profile-link {
        *zoom: 1;
        position: relative;
        display: block;
        background: #03556D;
        padding: 20px 10px;
    }

    .content>section.profile .profile-number .profile-link::after {
        content: '';
        display: block;
        clear: both;
    }

    .content>section.profile .profile-number .profile-link .profile_image {
        float: left;
        width: 60px;
        height: 60px;
        border-radius: 50%;
        overflow: hidden;
        vertical-align: top;
    }

    .content>section.profile .profile-number .profile-link .profile_image .icon-person {
        background: #e4e4e4;
        font-size: 62px;
    }

    .content>section.profile .profile-number .profile-link .user-info {
        float: left;
        margin-top: 8px;
        margin-left: 15px;
    }

    .content>section.profile .profile-number .profile-link .user-info p {
        font-weight: 700;
        font-size: 18px;
        color: #fff;
    }

    .content>section.profile .profile-number .profile-link .user-info p.user-info-top {
        padding-bottom: 8px;
    }

    .content>section.profile .profile-number .profile-link .user-info p .user-icon {
        display: inline-block;
        margin-left: -15px;
        margin-right: 5px;
        width: 20px;
        height: 20px;
    }

    .content>section.profile .profile-number .profile-link .user-info p .user-icon .icon-mobile {
        font-size: 30px;
        vertical-align: text-top;
    }

    .content>section.profile .profile-number .profile-link .user-info p .icon-mobile-number {
        font-size: 14px;
        color: #fff;
    }
    .icon-mobile-number{
        line-height: ;
    }
    .content>section.profile .profile-number .profile-link .arrow {
        width: 12px;
        height: 12px;
        position: absolute;
        right: 15px;
        top: 40%;
    }

    .content>section.profile .profile-number .profile-link .arrow .iconjiantou1 {
        color: #fff;
        font-size: 5px;
    }

    .content>section.profile .profile_info_data {
        position: relative;
        width: 100%;
        background: #fff;
        overflow: hidden;
    }

    .content>section.profile .profile_info_data::before {
        content: '';
        position: absolute;
        z-index: 200;
        left: 0;
        bottom: 0;
        width: 100%;
        height: 1px;
        background-color: #e4e4e4;
        transform: scaleY(0.5);
    }

    .content>section.profile .profile_info_data .info_data_list {
        *zoom: 1;
    }

    .content>section.profile .profile_info_data .info_data_list::after {
        content: '';
        display: block;
        clear: both;
    }

    .content>section.profile .profile_info_data .info_data_list .info_data_link {
        float: left;
        width: 33%;
        text-align: center;
        border-right: 1px solid #f1f1f1;
    }

    .content>section.profile .profile_info_data .info_data_list .info_data_link .info_data_top {
        display: block;
        width: 100%;
        font-size: 14px;
        color: #333;
        padding: 15px 5px 10px;
    }

    .content>section.profile .profile_info_data .info_data_list .info_data_link .info_data_top span {
        display: inline-block;
        font-size: 30px;
        color: #f90;
        font-weight: 700;
        line-height: 30px;
    }

    .content>section.profile .profile_info_data .info_data_list .info_data_link .info_data_bottom {
        display: inline-block;
        font-size: 14px;
        color: #666;
        font-weight: 400;
        padding-bottom: 10px;
    }

    .content>section.profile .profile_info_data .info_data_list .info_data_link:nth-of-type(2) .info_data_top span {
        color: #ff5f3e;
    }

    .content>section.profile .profile_info_data .info_data_list .info_data_link:nth-of-type(3) {
        border: 0;
    }

    .content>section.profile .profile_info_data .info_data_list .info_data_link:nth-of-type(3) .info_data_top span {
        color: #6ac20b;
    }

    .content>section.profile .profile_my_order {
        position: relative;
        margin-top: 10px;
        background: #fff;
    }

    .content>section.profile .profile_my_order::before {
        content: '';
        position: absolute;
        z-index: 200;
        left: 0;
        top: 0;
        width: 100%;
        height: 1px;
        background-color: #e4e4e4;
    }

    .content>section.profile .profile_my_order .my_order {
        display: flex;
        align-items: center;
        padding-left: 15px;
    }

    .content>section.profile .profile_my_order .my_order>span {
        display: flex;
        align-items: center;
        width: 20px;
        height: 20px;
    }

    .content>section.profile .profile_my_order .my_order>span>.iconfont {
        margin-left: -10px;
        font-size: 30px;
    }

    .content>section.profile .profile_my_order .my_order>span .icon-order-s {
        color: #03556D;
    }

    .content>section.profile .profile_my_order .my_order>span .icon-jifen {
        color: #ff5f3e;
    }

    .content>section.profile .profile_my_order .my_order>span .icon-vip {
        color: #f90;
    }

    .content>section.profile .profile_my_order .my_order>span .icon-fuwu {
        color: #03556D;
    }

    .content>section.profile .profile_my_order .my_order .my_order_div {
        width: 100%;
        border-bottom: 1px solid #f1f1f1;
        padding: 18px 10px 18px 0;
        font-size: 16px;
        color: #333;
        display: flex;
        justify-content: space-between;
    }

    .content>section.profile .profile_my_order .my_order .my_order_div span {
        display: block;
    }

    .content>section.profile .profile_my_order .my_order .my_order_div .my_order_icon {
        width: 10px;
        height: 10px;
    }

    .content>section.profile .profile_my_order .my_order .my_order_div .my_order_icon .iconjiantou1 {
        color: #bbb;
        font-size: 10px;
    }
</style>