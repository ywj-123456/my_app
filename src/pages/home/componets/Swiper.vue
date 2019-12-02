<template>
    <div class="wrapper">
        <swiper :options="swiperOption" v-if='List.length'>
        <swiper-slide v-for='item of list' :key='item.id'>
            <img class="swiper-img" src="item.imgUrl" alt="">
        </swiper-slide>
        <div class="swiper-pagination" slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
export default{
    name:'HomeSwiper',
    data(){
        return{
            swiperOption:{
                pagination:'.swiper-pagination',
                loop:true
            }
        }
    }
}
</script>
<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
   backgroud #fff
.wrapper
  overflow hidden
  width 100%
  height 0
  padding-bottom 26.66%
  .swiper-img
    width 100% 
</style>