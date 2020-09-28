<template>
    <div class="content">
        <section class="search">
            <HeaderTop title="搜索"></HeaderTop>
            <form class="search_form" action="#">
                <input type="search" name="search" placeholder="请输入商家或美食名称" class="search_input">
                <input type="submit" name="submit" class="search_submit">
            </form>
        </section>
    </div>
</template>

<script>
    import HeaderTop from '../../components/HeaderTop/HeaderTop.vue'
    export default {
        components: {
            HeaderTop
        }
    }
</script>

<style>
    .content>section.search {
        width: 100%;
    }
    .content>section.search .header{
        width: 100%;
        height: 45px;
        background-color: #03556D;
        text-align: center;
        line-height: 45px;
    }
    .content>section.search .header_title_text{
        color: white;
    }
    .content>section.search .search_form {
        *zoom: 1;
        background-color: #fff;
        margin-top: 45px;
        padding: 14px 5px;
    }

    .content>section.search .search_form::after {
        content: '';
        display: block;
        clear: both;
    }

    .content>section.search .search_form input {
        height: 35px;
        padding: 0 4px;
        border-radius: 2px;
        font-weight: bold;
        outline: none;
    }

    .content>section.search .search_form input.search_input {
        float: left;
        width: 79%;
        border: 4px solid #f2f2f2;
        font-size: 14px;
        color: #333;
        background-color: #f2f2f2;
    }

    .content>section.search .search_form input.search_submit {
        float: right;
        width: 20%;
        border: 4px solid #03556D;
        font-size: 16px;
        color: #fff;
        background-color: #03556D;
    }
</style>