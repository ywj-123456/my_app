<template>
    <div class="header">
        <div class="header-left">
             <span class="iconfont arrow-icon">&#xe609;</span>
        </div>
        <div class="header-input">
              <span class="iconfont">&#xe613;</span>
                 输入城市/景点/游玩主题
        </div>
        <!--使用router-link标签包裹header-right标签并制定路由跳转到'/city'-->
        <router-link to='/city'>
            <div class="header-right">
                <!-- {{this.city}} -->
                <!--使用vuex中的state里公用数据-->
                {{this.$store.state.city}}
                <!--传入城市的名称-->
                 <span class="iconfont arrow-icon">&#xe60c;</span>
            </div>
        </router-link>
     </div>
</template>

<script>
export default {
    name: 'HomeHeader',
    //使用vuex后就不在需要外部传递的city
    //props: {
    //  city: ""
    //}
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
  .header
    width 100%
    display: flex
    line-height: .88rem
    background: $bgColor
    color: #fff
    .header-left
      width: .64rem
      float: left
      .back-icon
        text-align: center
        font-size: .4rem
    .header-input
      flex: 1
      height: .64rem
      line-height: .64rem
      margin-top: .12rem
      margin-left: .2rem
      padding-left: .2rem
      background: #fff
      border-radius: .1rem
      color: #ccc
    .header-right
      min-width: 1.04rem
      padding: 0 .1rem
      float: right
      text-align: center
      color: #fff
      .arrow-icon
        margin-left: -.04rem
        font-size: .24rem
        
          
</style>