<template>
  <div id="app">
    <headerx></headerx>
    <bannerBox></bannerBox>
    <bannerBox2></bannerBox2>
    <section class="border-margin">
      <!-- <ul class="goodsList type1">
        <list1 v-for="(item,index) in listLen1"></list1>
      </ul>
      <ul class="goodsList type3">
        <list3 v-for="(item,index) in listLen3"></list3>
      </ul>
      <ul class="goodsList type2">
        <list2 v-for="(item,index) in listLen2"></list2>
      </ul> -->
      <ul1></ul1>
      <ul3></ul3>
      <ul2></ul2>
    </section>
    <turn></turn>
    <bannerBox2></bannerBox2>
    <ul2Custom1></ul2Custom1>
  </div>
</template>

<script>
import headerx from "./components/headerx.vue";
import ul1 from "./components/list/ul1.vue";
import ul2 from "./components/list/ul2.vue";
import ul3 from "./components/list/ul3.vue";
import turn from "./components/turn.vue";
import bannerBox from "./components/bannerBox.vue";
import bannerBox2 from "./components/bannerBox2.vue";
import ul2Custom1 from "./components/list/ul2-custom1.vue";





export default {
  name: 'App',
  data(){
    return{
    }
  },
  components:{headerx,ul1,ul2,ul3,turn,bannerBox,bannerBox2,ul2Custom1},
  mounted(){
    this.axios.get("/api/indexjson")
    .then(function(res){
      console.log(res)
    })
  }
}
</script>

<style lang="less">
header {
  height: .9rem;
  line-height: .9rem;
  font-size: .36rem;
  text-align: center;
}
.active-banner{
    width: 100%;
    background: #e6c387;
    border-bottom: .2rem solid #f5f5f5;
}
.active-banner>img,.custom-banner>img{
    width: 100%;
}
.custom-banner{
    width: 100%;
    background: #94d1a0;
}
.goodsList>li{
    box-sizing: border-box;
    // -moz-box-sizing: border-box;
    // -webkit-box-sizing: border-box;
    // -o-box-sizing: border-box;
    // -ms-box-sizing: border-box;  
    overflow: hidden;  
}
.goodsList.type1>li{
    width: 100%;
    padding: .3rem .4rem .3rem .3rem;
    border-bottom:1px solid #eee;
}
.goodsList .goodsImg{
    background: #eee;
}
.goodsInfo{
    position: relative;
}
.goodsList.type1 .goodsImg{
    width: 2.4rem;
    height: 2.4rem;
    margin-right:.2rem;
}
.goodsMark{
    overflow: hidden;
}
.goodsMark>li{
    float: left;
    font-size: .24rem;
    color:#999;
    width: 1.2rem;
    height: .36rem;
    line-height: .36rem;
    border: 1px solid #999;
    border-radius: .36rem;
    text-align: center;
    margin-right: .12rem;
}
.priceRow{
    position: absolute;
    bottom: 0.05rem;
    width: 100%;
    height: .36rem;
    overflow: hidden;
}
.priceRow>span:nth-child(1){
    color: #e71a41;
    font-size: .36rem;
    float: left;
    margin-right: .15rem;
}
.priceRow>span:nth-child(2){
    color: #999;
    font-size: .28rem;
    text-decoration: line-through;
    float: left;
    line-height: .45rem
}
.priceRow>span:nth-child(3){
    color: #999;
    font-size: .28rem;
    float:right;
    line-height: .45rem
}
.goodsList{
  overflow: hidden;
}
.goodsList.type3{
    border-bottom: 1px solid #eee;
    padding-top: .3rem;
}
.goodsList.type3 .goodsImg{
    width: 2.1rem;
    height: 2.1rem;
    background: #eee;
    margin-bottom: .2rem;
    margin: 0 auto;
    margin-bottom: .15rem;
}
.goodsList.type3>li{
    float: left;
    width: 33.33%;
        padding-bottom: .3rem;
}
.goodsList.type3 .goodsInfo{
    width: 2.1rem;
    margin: 0 auto;
}
.goodsList.type3 .priceRow{
    position: static;
    width: 2.1rem;
}
.goodsList.type3 .goodsInfo>p:first-child {
    text-overflow: ellipsis;
    overflow: hidden;
    display: -webkit-box;
    -webkit-line-clamp: 3;
    height: .9rem;
}
.goodsList.type2 {
    border-bottom: 1px solid #eee;
    padding-top: .3rem;
}
.goodsList.type2>li{
    float: left;
    width: 50%;
    padding-bottom: 4.8px;
    padding-bottom: .3rem;
}
.goodsList.type2>li .goodsImg{
    width: 3.3rem;
    height: 3.3rem;
    margin: 0 auto;
    margin-bottom: .15rem;
}
.goodsList.type2>li .goodsInfo{
    width: 3.3rem;
    margin: 0 auto;
}
.goodsList.type2>li .goodsInfo>p{
    text-overflow: ellipsis;
    overflow: hidden;
    display: -webkit-box;
    -webkit-line-clamp: 2;
    height: .6rem;
}
.goodsList.type2>li .priceRow{
    position: static;
}
.border-margin{
      border-bottom: .3rem solid #f5f5f5;
}
</style>
