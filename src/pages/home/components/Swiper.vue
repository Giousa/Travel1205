<template>

  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img"
             :src="item.imgUrl">
      </swiper-slide>

      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>

  </div>

</template>

<script>

export default {
  name: 'HomeSwiper',

  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1810/af/30ffcf34e9819f02.jpg_750x200_736b7236.jpg'
        },
        {
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1811/9d/a6e922acbb4c9802.jpg_750x200_74080b0c.jpg'
        },
        {
          id: '0003',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1805/e5/59fad13a64807d02.jpg_750x200_713ae984.jpg'
        }
      ]
    }
  }
}

</script>

<style scoped lang="stylus">

  .wrapper{
    width:100%;
    height:0;
    overflow: hidden;
    padding-bottom: 25%;
    background: #25a4bb;
  }
  .swiper-img{
    width:100%;
  }

  .wrapper >>> .swiper-pagination-bullet-active{
    background: #ffffff;
  }

</style>
