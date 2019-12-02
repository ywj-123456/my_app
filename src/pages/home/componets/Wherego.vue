<template>
    <div>
        <div class="title">
            <span class="title-content">周末去哪儿</span>
        </div>
        <ul>
            <li class="item" v-for='item of WheregoList' :key='item.id'>
                <img :src="item.imgUrl" alt="" class="item-img">
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
    name:'HomeWherego',
    data(){
        return{
            WheregoList:[{
                id:'001',
                imgUrl:'http://img1.qunarzz.com/sight/source/1711/2b/d4ebbd8337f1ac.jpg_r_640x214_2d4332c1.jpg',
                title:'湖南泡汤圣地',
                desc:'山谷幽深，泉水潺潺，宜人的自然风光，...'
            },{
                id:'002',
                imgUrl:'http://img1.qunarzz.com/sight/source/1509/3a/e163a8e32517d9.jpg_r_640x214_4fd882d3.jpg',
                title:'边城秋色',
                desc:'不得不看的边城秋日之美'
            },{
                id:'003',
                imgUrl:'http://img1.qunarzz.com/sight/source/1811/88/8d3b492ebf0b16.jpg_r_640x214_7b3a281d.jpg',
                title:'邂逅凤凰城',
                desc:'凤凰古城一个古老而神秘的地方，风景秀...'
            },{
                id:'004',
                imgUrl:'http://img1.qunarzz.com/sight/source/1811/b4/71c01c98139cf.jpg_r_640x214_30bac495.jpg',
                title:'亲身体验人间仙境',
                desc:'天桥天地，绝壁高崖之间的高台，台下深...'
            },{
                id:'005',
                imgUrl:'http://img1.qunarzz.com/sight/source/1812/1e/131ba1bc67be3e.jpg_r_640x214_edd2705d.jpg',
                title:'株洲必打卡',
                desc:'亲身体验株洲当地人最爱的去处'
            }]
        }
    }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl';
  .title
    margin-top .1rem
    background #eee
    padding .2rem
   .title-content
     margin-left: .08rem
     height: .44rem
     color: black
     font-size: .30rem
     line-height: .44rem
  .item
    padding-bottom .3rem
    .item-img
      width 100%
     .item-info
       margin-left .2rem
       margin-top .2rem
       .item-title
         font-size .28rem
       .item-desc
          color #999
          font-size .20rem
          margin-top .1rem
</style>