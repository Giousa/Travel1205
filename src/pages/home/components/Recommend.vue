<template>

  <div>
    <div class="recommend-title">热销推荐</div>

    <ul>
      <li class="item border-bottom" v-for="item of list"  :key="item.id">
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
  props: {
    list: Array
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
