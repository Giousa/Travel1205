<template>

  <div>
    <div class="recommend-title">热销推荐</div>

    <ul>
      <li class="item border-bottom" v-for="item of recommendList"  :key="item.id">
          <div>
            <img class="item-img" :src='item.imgUrl'>
          </div>

          <div class="item-info">
            <p class="item-title">{{item.title}}</p>
            <p class="item-desc">{{item.desc}}</p>
            <button class="item-button">查看详情</button>
          </div>
      </li>

    </ul>

  </div>
</template>

<script>

export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/7c/7cda8b6782dabd80b4.img.jpg_200x200_2039e660.jpg',
          title: '上海迪士尼乐园',
          desc: '上海迪士尼乐园热烈欢迎甜腻腻'
        },
        {
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/7c/7cda8b6782dabd80b4.img.jpg_200x200_2039e660.jpg',
          title: '上海迪士尼乐园',
          desc: '上海迪士尼乐园热烈欢迎甜腻腻'
        },
        {
          id: '0003',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/7c/7cda8b6782dabd80b4.img.jpg_200x200_2039e660.jpg',
          title: '上海迪士尼乐园',
          desc: '上海迪士尼乐园热烈欢迎甜腻腻'
        },
        {
          id: '0004',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/7c/7cda8b6782dabd80b4.img.jpg_200x200_2039e660.jpg',
          title: '上海迪士尼乐园',
          desc: '上海迪士尼乐园热烈欢迎甜腻腻'
        },
        {
          id: '0005',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/7c/7cda8b6782dabd80b4.img.jpg_200x200_2039e660.jpg',
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
    margin-top: .2rem;
    line-height: .8rem;
    background: #ccc;
    text-indent: .2rem;
    text-align: left;
  }

  .item{
    display: flex;
    height: 1.9rem;
    overflow: hidden;
  }

  .item-img{
    width: 1.7rem;
    height: 1.7rem;
    padding: .1rem;
  }

  .item-info{
    flex: 1;
    text-align: left;
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

  .item-button{
    line-height: .44rem;
    margin-top: .1rem;
    background: #ff9300;
    padding: .1rem;
    border-radius: .06rem;
  }
</style>
