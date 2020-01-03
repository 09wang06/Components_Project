<template>
    <div>
        <div class="title">热门推荐</div>
        <ul class="menu">
            <li @click="menu01">笔记本电脑</li>
            <li @click="menu02">零食</li>
            <li @click="menu03">手表</li>
            <li @click="menu04">书籍</li>
            <li @click="menu05">家电</li>
            <li @click="menu06">服饰</li>
            <li @click="menu07">学习用品</li>
            <li @click="menu08">新品5G手机</li>
            <li @click="menu09">办公用品</li>
            <li @click="menu10">游戏充值</li>
            <li @click="menu11">旅游出行</li>
        </ul>
    </div>
</template>

<script>
    import Msg from './msg.js';
    
    export default {
       methods:{
           menu01:function (){
                Msg.$emit("value","1");
           },
           menu02:function (){
                Msg.$emit("value","2");
           },
           menu03:function (){
                Msg.$emit("value","3");
           },
           menu04:function (){
                Msg.$emit("value","4");
           },
           menu05:function (){
                Msg.$emit("value","5");
           },
           menu06:function (){
                Msg.$emit("value","6");
           },
           menu07:function (){
                Msg.$emit("value","7");
           },
           menu08:function (){
                Msg.$emit("value","8");
           },
           menu09:function (){
                Msg.$emit("value","9");
           },
           menu10:function (){
                Msg.$emit("value","10");
           },
           menu11:function (){
                Msg.$emit("value","11");
           },
       } 
    }
</script>

<style scoped>
    .title {
        width: 100px;
        color: red;
    }

    .menu li{
        list-style-type: none;
        height: 50px;
        margin-bottom: 2px;
        background-color: white;
        line-height: 50px;
        cursor: pointer;
    }
</style>

