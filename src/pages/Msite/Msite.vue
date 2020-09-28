<template>
    <div class="content">
        <section class="msite">
            <!--首页头部-->
            <HeaderTop :title='title'>
                <span class="header_search" slot="left">
                    <i class="iconfont iconsearch" style="color: white; font-size: 20px"></i>
                </span>
                <span class="header_login" slot="right">
                    <span class="header_login_text">登录 | 注册</span>
                </span>
            </HeaderTop>
            <!--首页导航-->
            <nav class="msite_nav">
                <div class="swiper-container">
                    <div class="swiper-wrapper">
                        <div class="swiper-slide">
                            <a href="javascript:" class="link_to_food">
                                <div class="food_container">
                                    <img src="./images/nav/1.jpg">
                                </div>
                                <span>甜品饮品</span>
                            </a>
                            <a href="javascript:" class="link_to_food">
                                <div class="food_container">
                                    <img src="./images/nav/2.jpg">
                                </div>
                                <span>商超便利</span>
                            </a>
                            <a href="javascript:" class="link_to_food">
                                <div class="food_container">
                                    <img src="./images/nav/3.jpg">
                                </div>
                                <span>美食</span>
                            </a>
                            <a href="javascript:" class="link_to_food">
                                <div class="food_container">
                                    <img src="./images/nav/4.jpg">
                                </div>
                                <span>简餐</span>
                            </a>
                            <a href="javascript:" class="link_to_food">
                                <div class="food_container">
                                    <img src="./images/nav/5.jpg">
                                </div>
                                <span>新店特惠</span>
                            </a>
                            <a href="javascript:" class="link_to_food">
                                <div class="food_container">
                                    <img src="./images/nav/6.jpg">
                                </div>
                                <span>准时达</span>
                            </a>
                            <a href="javascript:" class="link_to_food">
                                <div class="food_container">
                                    <img src="./images/nav/7.jpg">
                                </div>
                                <span>预订早餐</span>
                            </a>
                            <a href="javascript:" class="link_to_food">
                                <div class="food_container">
                                    <img src="./images/nav/8.jpg">
                                </div>
                                <span>土豪推荐</span>
                            </a>
                        </div>
                        <div class="swiper-slide">
                            <a href="javascript:" class="link_to_food">
                                <div class="food_container">
                                    <img src="./images/nav/9.jpg">
                                </div>
                                <span>甜品饮品</span>
                            </a>
                            <a href="javascript:" class="link_to_food">
                                <div class="food_container">
                                    <img src="./images/nav/10.jpg">
                                </div>
                                <span>商超便利</span>
                            </a>
                            <a href="javascript:" class="link_to_food">
                                <div class="food_container">
                                    <img src="./images/nav/11.jpg">
                                </div>
                                <span>美食</span>
                            </a>
                            <a href="javascript:" class="link_to_food">
                                <div class="food_container">
                                    <img src="./images/nav/12.jpg">
                                </div>
                                <span>简餐</span>
                            </a>
                            <a href="javascript:" class="link_to_food">
                                <div class="food_container">
                                    <img src="./images/nav/13.jpg">
                                </div>
                                <span>新店特惠</span>
                            </a>
                            <a href="javascript:" class="link_to_food">
                                <div class="food_container">
                                    <img src="./images/nav/14.jpg">
                                </div>
                                <span>准时达</span>
                            </a>
                            <a href="javascript:" class="link_to_food">
                                <div class="food_container">
                                    <img src="./images/nav/1.jpg">
                                </div>
                                <span>预订早餐</span>
                            </a>
                            <a href="javascript:" class="link_to_food">
                                <div class="food_container">
                                    <img src="./images/nav/2.jpg">
                                </div>
                                <span>土豪推荐</span>
                            </a>
                        </div>
                    </div>
                    <!-- Add Pagination -->
                    <div class="swiper-pagination"></div>
                    <!-- <div class="swiper-scrollbar"></div> -->
                </div>
            </nav>
            <!--首页附近商家-->
            <ShopList></ShopList>
            
        </section>
    </div>
</template>

<script>
    import HeaderTop from '../../components/HeaderTop/HeaderTop.vue'
    import Swiper from 'swiper'
    import ShopList from '../../components/ShopList/ShopList.vue'

    export default {
        mounted() {
            //创建swiper实例对象 来实现轮播图
            var mySwiper = new Swiper('.swiper-container', {

                loop: true, // 循环模式选项
                // 如果需要分页器
                pagination: {
                    el: '.swiper-pagination',
                },
                
                // // 如果需要前进后退按钮
                // navigation: {
                //     nextEl: '.swiper-button-next',
                //     prevEl: '.swiper-button-prev',
                // },

                // // 如果需要滚动条
                // scrollbar: {
                //     el: '.swiper-scrollbar',
                // },
            })
        },
        components: {
            HeaderTop,
            ShopList
        },
        data() {
            return {
                title: '华中师范大学南湖校区'
            }
        },
    }
</script>

<style>
    @import url('//at.alicdn.com/t/font_2080100_szw8g5bj2z.css');
    @import 'swiper/swiper-bundle.min.css';

    .content>section.msite {
        width: 100%;
    }

    .content>section.msite .msite_nav {
        position: relative;
        margin-top: 45px;
        height: 200px;
        background: #fff;
    }

    .content>section.msite .msite_nav::before {
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

    .content>section.msite .msite_nav .swiper-container {
        width: 100%;
        height: 100%;
    }

    .content>section.msite .msite_nav .swiper-container .swiper-wrapper {
        width: 100%;
        height: 100%;
    }

    .content>section.msite .msite_nav .swiper-container .swiper-wrapper .swiper-slide {
        display: flex;
        justify-content: center;
        align-items: flex-start;
        flex-wrap: wrap;
    }

    .content>section.msite .msite_nav .swiper-container .swiper-wrapper .swiper-slide .link_to_food {
        width: 25%;
    }

    .content>section.msite .msite_nav .swiper-container .swiper-wrapper .swiper-slide .link_to_food .food_container {
        display: block;
        width: 100%;
        text-align: center;
        padding-bottom: 10px;
        font-size: 0;
    }

    .content>section.msite .msite_nav .swiper-container .swiper-wrapper .swiper-slide .link_to_food .food_container img {
        display: inline-block;
        width: 50px;
        height: 50px;
    }

    .content>section.msite .msite_nav .swiper-container .swiper-wrapper .swiper-slide .link_to_food span {
        display: block;
        width: 100%;
        text-align: center;
        font-size: 13px;
        color: #666;
    }

    .content>section.msite .msite_nav .swiper-container .swiper-pagination>span.swiper-pagination-bullet-active {
        background: #03556D;
    }
</style>