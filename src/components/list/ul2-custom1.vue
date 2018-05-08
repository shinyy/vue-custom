<template>
    <ul class="goodsList type2">
        <list2 v-for="{li,index} in listLen"></list2>
    </ul>
</template>
<script>
import list2 from "./list2.vue";
export default {
    data(){
      return{
          listLen:5
      }
  },
  components:{list2}
}
</script>

