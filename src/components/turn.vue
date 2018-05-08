<template>
  <section class="turn border-margin">
      <p class="cusTil">{{turnTil}}</p>
      <div class="swiper-container">
        <div class="swiper-wrapper">
            <div class="swiper-slide" style="background:#f60"></div>
            <div class="swiper-slide" style="background:#17a7d0"></div>
            <div class="swiper-slide" style="background:#ccc"></div>
            <div class="swiper-slide" style="background:#f60"></div>
            <div class="swiper-slide" style="background:#17a7d0"></div>
            <div class="swiper-slide" style="background:#ccc"></div>
        </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
        turnTil:"自定义分类标题"
    };
  },
  //写方法
  methods: {
    instantiation: function() {
    //   var swiper = new Swiper(".swiper-container", {
    //         pagination: ".swiper-pagination",
    //         paginationClickable: true,
    //         autoplay: 2500,
    //         autoplayDisableOnInteraction: false,
    //         loop: true,
    //         onSlideChangeEnd: function(swiper) {
    //             $(".activeIndex").text(swiper.activeIndex);
    //         }
    //     });
    var swiper = new Swiper('.swiper-container', {
        pagination: '.swiper-pagination',
        slidesPerView: 3,
        paginationClickable: true,
        spaceBetween: 15,
        freeMode: true
    });
    }
  },
  //执行方法 还可以写成 mounted:function(){}
  mounted() {
    this.instantiation();
  }
};
</script>

<style>
.swiper-wrapper {
  max-width: 7.5rem;
  height: 2.6rem;
}
.swiper-wrapper img {
  width: 100%;
  height: 4.21875rem;
}
.turn{
    width: 7.5rem;
    padding: .25rem 0 .5rem 0;
    box-sizing: border-box;
}
.cusTil{
    text-align: center;
    font-size: .32rem;
    margin-bottom: .3rem;
}
.swiper-slide{
    width: 2.1rem;
    height: 2.6rem;
    border-radius: .06rem;
    overflow: hidden;
}
</style>
