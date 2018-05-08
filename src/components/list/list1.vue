<template>
            <li @click="tap">
                <a href="#" class="y-flex">
                    <div class="goodsImg"><img src="" /></div>
                    <div class="goodsInfo flex1">
                        <p class="fz26 c333 lh32 bmar15">漫步者（EDIFIER）H293P 杀手级手机入耳式耳机耳塞 黑</p>
                        <ul class="goodsMark">
                            <li>99包邮</li>
                            <li>买三赠一</li> 
                            <li>{{test}}</li>                            
                                                       
                        </ul>
                        <div class="priceRow">
                            <span>￥199</span>
                            <span>￥299</span>
                            <span>已售9999件</span>
                        </div>
                    </div>
                </a>
            </li>
</template>
<script>
export default {
  data(){
      return{
         test:"测试",
         listLen:5
      }
  },
  methods:{
      tap:function(){
          alert(11)
      }
  }
}
</script>
<style lang="less" scoped>

</style>
