<template>
    <div class="content">
        <section class="order">
            <HeaderTop title="订单列表"></HeaderTop>
                <section class="order_no_login">
                    <img src="./images/person.png">
                    <h3>登录后查看外卖订单</h3>
                    <button @click = "goTo('/Login')">立即登陆</button>
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
    .content>section.order {
        width: 100%;
    }

    .content>section.order .header {
        width: 100%;
        height: 45px;
        background-color: #03556D;
        text-align: center;
        line-height: 45px;
    }

    .content>section.order .order_no_login {
        padding-top: 140px;
        width: 60%;
        margin: 0 auto;
        text-align: center;
    }

    .content>section.order .order_no_login>img {
        display: block;
        width: 100%;
        height: 30%;
    }

    .content>section.order .order_no_login>h3 {
        padding: 10px 0;
        font-size: 17px;
        color: #6a6a6a;
    }

    .content>section.order .order_no_login>button {
        display: inline-block;
        background: #03556D;
        font-size: 14px;
        color: #fff;
        border: 0;
        outline: none;
        border-radius: 5px;
        padding: 10px 20px;
    }
</style>