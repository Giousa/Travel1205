<template>

  <div>
    <div class="recommend-title">周末去哪儿</div>

    <ul>
      <li class="item border-bottom" v-for="item of recommendList"  :key="item.id">
          <div class="item-img-wrapper">
            <img class="item-img" :src='item.imgUrl'>
          </div>

          <div class="item-info">
            <p class="item-title">{{item.title}}</p>
            <p class="item-desc">{{item.desc}}</p>
          </div>
      </li>

    </ul>

  </div>
</template>

<script>

export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1505/7d/df6ff468331c43.jpg_r_640x214_1f3783d0.jpg',
          title: '上海迪士尼乐园',
          desc: '上海迪士尼乐园热烈欢迎甜腻腻'
        },
        {
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1505/7d/df6ff468331c43.jpg_r_640x214_1f3783d0.jpg',
          title: '上海迪士尼乐园',
          desc: '上海迪士尼乐园热烈欢迎甜腻腻'
        },
        {
          id: '0003',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1505/7d/df6ff468331c43.jpg_r_640x214_1f3783d0.jpg',
          title: '上海迪士尼乐园',
          desc: '上海迪士尼乐园热烈欢迎甜腻腻'
        },
        {
          id: '0004',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1505/7d/df6ff468331c43.jpg_r_640x214_1f3783d0.jpg',
          title: '上海迪士尼乐园',
          desc: '上海迪士尼乐园热烈欢迎甜腻腻'
        },
        {
          id: '0005',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1505/7d/df6ff468331c43.jpg_r_640x214_1f3783d0.jpg',
          title: '上海迪士尼乐园',
          desc: '上海迪士尼乐园热烈欢迎甜腻腻'
        }
      ]
    }
  }
}

</script>

<style scoped>

  .recommend-title {
    line-height: .8rem;
    background: #ccc;
    text-indent: .2rem;
    text-align: left;
  }

  .item-img{
    width: 100%;
  }

  .item-info{
    padding: .1rem;
    min-width: 0;
  }

  .item-title{
    line-height: .54rem;
    font-size: .32rem;
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
  }

  .item-desc{
    line-height: .4rem;
    color: #ccc;
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
  }

  .item-img-wrapper{
    overflow: hidden;
    height:0;
    padding-bottom: 33.9%;
  }
</style>
