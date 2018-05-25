<template>
  <div id="rating">
    <h1 class="rating-title">用户评价</h1>
    <swiper :options="swiperOption">
      <swiper-slide v-for="item in userList">
        <div class="rating-wrapper">
          <div class="rating-item">
            <div class="item-pic"></div>
            <div class="item-cont">
              <h2 class="item-cont-name">{{item.name}}</h2>
              <h3 class="item-cont-title">{{item.title}}</h3>
              <span class="item-cont-detail">{{item.detail}}</span>
            </div>
          </div>
        </div>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
  export default {
    name: 'HomeRating',
    data() {
      return {
        userList: [
          {
            name: '刘作晓',
            title: '法务VC联合创始人',
            detail: '我在阿里巴巴工作十年，2014年创立荷马金融海外理财平台，专为中高净值人群优选海外金融资产，权大师的知识产权服务为我们的涉外业务提供了有力的保障，非常感谢！',
          },
          {
            name: '张近',
            title: '微软技术专家',
            detail: '权大师提供的知识产权保护及相关服务，为创业者提供了全方位的支持，在这个传统的不能再传统的行业里，用全新的互联网模式，解析了互联网人对于改变传统服务行业现状的渴望，相信会创造出非凡的成就。',
          },
          {
            name: '赵勇',
            title: '百度前端Leader',
            detail: '作为国内最大的环保创意类纸家具设计、生产厂家，要成就中国自己的原创微奢品牌，知识产权的保护是重中之重，权大师专业、高效和良好的服务素养令我非常满意！',
          },
        ],
        swiperOption: {
          speed:2200,
          // 分页器
          pagination: {
            el: '.swiper-pagination',
            type: 'bullets',
            clickable :true,
          },
          // 切换效果
          effect : 'fade',
          fadeEffect: {
            crossFade: true,
          },
          loop: true,
          autoplay: {
            delay: 3000,  // 3秒切换一次
            stopOnLastSlide: false,
            disableOnInteraction: false,
          },
        }
      }
    }
  }
</script>

<style>
  #rating .swiper-pagination-bullets {
    bottom: 50px!important;
  }

  #rating .swiper-pagination-bullet {
    width: 14px!important;
    height: 14px!important;
    background-color: #7e7d7d!important;
    border-radius: 50%!important;
    margin: 0 10px!important;
  }

  #rating .swiper-pagination-bullet-active {
    background-color: #ff7f00!important;
  }

 #rating {
   padding: 70px 0 60px;
   width: 1200px;
   margin: 0 auto;
   border-bottom: solid 1px #eee;
 }

 #rating .rating-wrapper {
   padding-bottom: 100px;
 }

 .rating-title {
   font-size: 26px;
 }

 .rating-item {
   margin: 0 125px;
   margin-top: 80px;
   display: flex;
 }

 .rating-item .item-pic {
   width: 180px;
   height: 180px;
   border-radius: 50%;
   background: lightblue;
 }

 .rating-item .item-cont {
   width: 615px;
   height: 200px;
   margin-left: 100px;
   overflow: hidden;
 }

 .rating-item .item-cont .item-cont-name {
   font-size: 26px;
 }

 .rating-item .item-cont .item-cont-title {
   font-size: 20px;
   color: #555;
   margin-top: 6px;
   margin-bottom: 32px;
 }

 .rating-item .item-cont .item-cont-detail {
   font-size: 14px;
   color: #999;
   line-height: 22px;
 }

</style>
