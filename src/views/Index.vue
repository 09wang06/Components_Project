<template>
    <div class="main">
        <div class="left">
            <Left></Left>
        </div>

        <div class="right">
            <div class="top">
                <img src="img/title.jpg">
            </div>

            <div class="buttom">
                <Right></Right>
            </div>
        </div>
    </div>
</template>

<script type="text/javascript">
    
    import Left from '../components/left.vue'
    import Right from '../components/right.vue'

    export default{
        components:{
            Left,
            Right
        }
    }
    
</script>>


<style >

    *{
        padding: 0;
        margin: 0;
    }

    .left{
        width: 150px;
        float: left;
        margin-right: 10px;

    }

    .right{
        width: 1000px;
        float: left;
        margin-left: 10px;

    }

    .main{
        width: 1200px;
        margin: 20px auto;

    }

    .top img{
        height: 200px;
        width: 1000px;

    }

    .left,.right{
        background: #f5f5f5;
        height: 500px;
    }
</style>