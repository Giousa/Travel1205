<template>
  <div class="icons">

    <swiper>
      <swiper-slide v-for="(page,index) of pages" :key="index">

        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-content" :src='item.imgUrl'/>
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>

  </div>
</template>

<script>

export default {
  name: 'HomeIcons',
  props: {
    list: Array
  },
  computed: {

    pages () {
      const pages = []
      this.list.forEach(function (item, index) {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}

</script>

<style scoped lang="stylus">

  @import '~styles/mixins.styl'

  .icons{
    margin-top: .2rem;
    overflow: hidden;
    height:0;
    padding-bottom:50%;

  }

  .icon{
    position: relative;
    overflow: hidden;
    float: left;
    width:25%;
    height:0;
    padding-bottom: 25%;
  }

  .icon-img{
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom:.44rem;
  }

  .icon-img-content{
    height:100%;
    margin: 0 auto;
    display: block;
  }

  .icon-desc{
    position: absolute;
    left: 0;
    right: 0;
    bottom:.10rem;
    line-height: .44rem;
    color: #333;
    ellipsis()
  }

  .swiper-container{
    height:0;
    padding-bottom:50%;
  }
</style>
