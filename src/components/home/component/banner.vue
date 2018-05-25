<template>
  <div id="banner">
    <swiper :options="swiperOption">
      <swiper-slide
      class="swiper-img"
      v-for="imgUrl in swiperImg"
      :style="{backgroundImage:`url(${imgUrl})`}">
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
  export default {
    name: 'HomeBanner',
    data() {
      return {
        swiperImg: [
          "https://tm-files.oss-cn-beijing.aliyuncs.com/ad/2018/04/27/c7e22c9f90298929e48a8dced4e349d2.png",
          "https://tm-files.oss-cn-beijing.aliyuncs.com/ad/2018/04/20/154b41efc4b0aa7e560f5f9f6fae7e66.jpg",
        ],
        swiperOption: {
          pagination: {
            el: '.swiper-pagination',
            type: 'bullets',
            clickable :true,
          },
          loop: true,
          autoplay: {
            delay: 3000,  // 3秒切换一次
            stopOnLastSlide: false,
            disableOnInteraction: false,
          },
        }
      }
    },
  }
</script>

<style>
  #banner .swiper-pagination-bullet {
   width: 14px!important;
   height: 14px!important;
   background-color: #333!important;
   opacity: .8!important;
   border-radius: 50%!important;
   margin: 0 5px!important;
  }

  #banner .swiper-pagination-bullet-active {
   background-color: #fff!important;
  }

  #banner {
    overflow: hidden;
    width: 100%;
    min-width: 1200px;
    background: #eee;
  }

  .swiper-container {
    height: 498px;
  }

  .swiper-img {
    width: 100%;
    height: 100%;
    background-position: center 0;
    background-repeat: no-repeat;
  }
</style>
