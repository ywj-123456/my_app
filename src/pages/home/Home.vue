<template>
     <div>
        <home-header></home-header>
        <home-swiper></home-swiper>
        <home-icons></home-icons>
        <home-hot></home-hot>
        <home-wherego></home-wherego>
    </div>
</template>

<script>
import HomeHeader from './componets/header'
import HomeSwiper from './componets/Swiper'
import HomeIcons from './componets/Icons'
import HomeHot from './componets/Hot'
import HomeWherego from './componets/Wherego'
export default{
    name: 'Home',
    components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeHot,
    HomeWherego
  }
}
</script>

<style scoped>
</style>