<template>
     <div>
        <home-header></home-header>
        <home-swiper></home-swiper>
        <home-icons></home-icons>
        <home-hot></home-hot>
    </div>
</template>

<script>
import HomeHeader from './componets/header'
import HomeSwiper from './componets/Swiper'
import HomeIcons from './componets/Icons'
import HomeHot from './componets/Hot'
export default{
    name: 'Home',
    components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeHot
  }
}
</script>

<style scoped>
</style>