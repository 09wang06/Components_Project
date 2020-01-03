<template>
    <div name="show">
        <ul class="ProList">
            <li v-for="pro in list" >
                <img v-bind:src="pro.img">
                <p>{{pro.proName}}</p>
            </li>
        </ul>
    </div>
</template>

<script>

    export default {
       name:"show",
       data(){//初始化
            var _this = this;
            this.$axios.get("json/bjb.json").then(function(res){
                _this.list = res.data;
            });
            return {
                list:[]
            }
       },
       props:{//传参
           proId : Number,
       },
       watch:{//监听
           proId(){
               var _this = this;
               var url = "";
               if(_this.proId == 1){
                   url = "json/bjb.json";
               }else if(_this.proId == 2){
                   url = "json/food.json";
               };

                this.$axios.get(url).then(function(res){
                    _this.list = res.data;
                });
                return {
                    list:[]
                }
           }
       }
    }
</script>

<style >
    .ProList li{
        width: 200px;
        height: 200px;
        list-style: none;
        float: left;
        font-size: 9px;
        color: red;
        margin-bottom: 30px;
    }

    .ProList img{
        width: 180px;
        height: 180px;
    }
</style>