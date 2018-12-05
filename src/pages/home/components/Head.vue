<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont backicon">&#xe624;</span>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩主题
    </div>
    <div class="header-right">
      {{this.city}}
      <span class="iconfont arrowicon">&#xe64a;</span>
    </div>
  </div>
</template>

<script>

export default {

  name: 'HomeHeader',
  props: {
    city: String
  }
}

</script>

<style lang="stylus" scoped>

  @import '~styles/varibles.styl';

  .header {
    display: flex;
    line-height: .86rem;
    background: $bgColor;
    color: #fff;
  }

  .header-left {
    width: .64rem;
    float: left;
  }

  .header-right {
    width: 1.24rem;
    float: right;
    text-align: center;
  }

  .header-input {
    text-align: left;
    flex: 1;
    background: #ffffff;
    border-radius: .1rem;
    color: #ccc;
    height: .64rem;
    line-height: .64rem;
    margin-top: .12rem;
    margin-left: .2rem;
    padding-left: .2rem;
  }

  .iconfont.backicon{
    text-align: center;
    font-size: .4rem;
  }

  .iconfont.arrowicon{
    font-size: .2rem;
  }
</style>
