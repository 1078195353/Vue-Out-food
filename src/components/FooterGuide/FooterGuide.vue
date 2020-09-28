<template>
    <div class="footer_guide border-1px">
        <a href="javascript:;" class="guide_item" :class="{on: '/msite' ===$route.path }" @click="goTo('/msite')">
            <span class="item_icon" >
                <i  class="iconfont iconu"></i>
            </span>
            <span>外卖</span>
        </a>
        <a href="javascript:;" class="guide_item" :class="{on: '/search' ===$route.path }"  @click="goTo('/search')" >
            <span class="item_icon">
                <i class="iconfont iconsousuo"></i>
            </span>
            <span>搜索</span>
        </a>
        <a href="javascript:;" class="guide_item" :class="{on: '/order' ===$route.path }"  @click="goTo('/order')" >
            <span class="item_icon">
                <i class="iconfont icondingdan"></i>
            </span>
            <span>订单</span>
        </a>
        <a href="javascript:;" class="guide_item" :class="{on: '/profile' ===$route.path }" @click="goTo('/profile')" >
            <span class="item_icon">
                <i class="iconfont icongeren1"></i>
            </span>
            <span>我的</span>
        </a>
    </div>
</template>

<script>
    export default {
        methods: {
            goTo(path){
                this.$router.replace(path)
            }
        },
    }
</script>

<style>
    @import url('//at.alicdn.com/t/font_2080100_1st7os299td.css');
    .footer_guide {
        position: relative;
        position: fixed;
        z-index: 100;
        left: 0;
        right: 0;
        bottom: 0;
        background-color: #fff;
        width: 100%;
        height: 50px;
        display: flex;
    }

    .footer_guide::before {
        content: '';
        position: absolute;
        z-index: 200;
        left: 0;
        top: 0;
        width: 100%;
        height: 1px;
        background-color: #e4e4e4;
    }

    .footer_guide .guide_item {
        display: flex;
        flex: 1;
        text-align: center;
        flex-direction: column;
        align-items: center;
        margin: 5px;
        color: #999;
    }

    .footer_guide .guide_item.on {
        color: #03556D;
    }

    .footer_guide .guide_item span {
        font-size: 14px;
        margin-top: 2px;
        margin-bottom: 2px;
    }

    .footer_guide .guide_item span .iconfont {
        font-size: 22px;
    }
</style>