<template>
    <div>
        <!-- 根据kk的值，判断点击的是哪个菜单项 -->
        <div v-if="kk==1">
            <ProList :proId="1"></ProList>
        </div>
        <div v-if="kk==2">
            <ProList :proId="2"></ProList>
        </div>
        <div v-if="kk==3">
            <ProList :proId="3"></ProList>
        </div>
        <div v-if="kk==4">
            <ProList :proId="4"></ProList>
        </div>
    </div>
</template>

<script>
    import Msg from './msg.js';
    import ProList from './proList.vue';

    export default {
        data(){
            return {//默认显示“笔记本电脑信息”
                kk : 1,
            }
        },
        mounted : function(){
            var _this = this;

            Msg.$on('value', function(m){//接收传参m
                _this.kk = m;
            })
        },
        components:{//定义组件ProList
            ProList
        }
    }
</script>