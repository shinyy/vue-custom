<template>
    <ul class="goodsList type1">
        <list1 v-for="{li,index} in listLen"></list1>
    </ul>
</template>
<script>
import list1 from "./list1.vue";
export default {
  data(){
      return{
          listLen:2
      }
  },
  components:{list1}
}
</script>

