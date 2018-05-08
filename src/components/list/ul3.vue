<template>
    <ul class="goodsList type3">
        <list3  v-for="{li,index} in listLen"></list3>
    </ul>
</template>
<script>
import list3 from "./list3.vue";
export default {
    data(){
      return{
          listLen:3
      }
  },
  components:{list3}
}
</script>

