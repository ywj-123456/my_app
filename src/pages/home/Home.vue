<template>
     <div>
        <home-header :city='city'></home-header>
        <home-swiper :list='swiperList'></home-swiper>
        <home-icons :list='iconList'></home-icons>
        <home-hot :list='hotList'></home-hot>
        <home-liked :list='likedList'></home-liked>
        <home-wherego :list='wheregoList'></home-wherego>
    </div>
</template>

<script>
import HomeHeader from './componets/header'
import HomeSwiper from './componets/Swiper'
import HomeIcons from './componets/Icons'
import HomeHot from './componets/Hot'
import HomeLiked from './componets/Liked'
import HomeWherego from './componets/Wherego'
import axios from 'axios'
export default{
    name: 'Home',
    components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeHot,
    HomeLiked,
    HomeWherego
  },
  data(){
    return{
      city:'',
      swiperList:[],
      iconList:[],
      hotList:[],
      likeList:[],
      wheregoList:[]
    }
  },
  methods:{
    getHomeInfo(){
      axios.get('./api/index.json').then(this.getHomeInfoSUcc)
    },
    getHomeInfoSucc(res){
      res=res.data
      if(res.ret && res.data){
        const data=res.data
        this.city=data.city
        this.swiperList=data.swiperList
        this.iconList=data.iconList
        this.hotList=data.hotList
        this.likeList=data.likeList
        this.wheregoList=data.wheregoList
      }
    }
  },
  mounted(){
    this.getHomeInfo()
  }
}
</script>

<style scoped>
</style>