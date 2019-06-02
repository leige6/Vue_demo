<template>
 <div class="recom">
   <div class="icons-down">
     <div class="icons-left border-right"><span class="iconfont map-icon">&#xe61b;</span>定位失败</div>
     <div class="icons-right"> <span class="iconfont map-icon">&#xe719;</span>必游榜单</div>
   </div>
   <div class="recom-content">
     <div class="title">
       <span class="iconfont like-icon"> &#xe64e;</span> 猜你喜欢
     </div>
     <ul>
       <li>
         <div class="item">
           <img class="item-img" src="http://img1.qunarzz.com/sight/p0/1411/43/dea8b51719a4a69b68777baa68c146e4.water.jpg_200x200_8da8cebe.jpg" alt="">
           <div class="item-right">
             <p class="name">春晖园温泉度假村</p>
             <p class="comment">1027条评论</p>
             <p class="price"><span class="price-currency">￥<em class="price-num">170</em></span>起</p>
           </div>
         </div>
       </li>
     </ul>
   </div>
 </div>
</template>

<script>
export default {
  name: 'HomeRecommend'
}
</script>

<style lang="stylus" scoped>
.recom
  background-color #EEE
  .icons-down
    display flex
    height 0.98rem
    background-color #FFF
    .map-icon
      font-size .4rem
      margin-right .05rem
    .icons-left
      text-align center
      flex 1
      line-height 0.98rem
    .icons-right
      flex 1
      text-align center
      line-height 0.98rem
  .recom-content
    margin-top .17rem
    background-color #FFF
    .title
      height .95rem
      line-height .95rem
      padding-left .2rem
      padding-right .2rem
      .like-icon
        font-size .4rem
        color #ff7e46
  .item
    height 2.4rem
    display flex
    .item-img
      width 2rem
      height 2rem
      padding .2rem
    .item-right
      flex 1
      padding .2rem .2rem .2rem 0
      .name
        //font-weight bold
        font-size 0.32rem
        margin-top 0.26rem
        height 0.44rem
        line-height 0.44rem
      .comment
        margin-top .14rem
        line-height .34rem
        color #616161
        vertical-align text-bottom
      .price
        margin-top: .22rem;
        color: #616161;
        font-size .24rem;
        line-height: .4rem;
        .price-currency
          color #FF8300
          .price-num
            font-size .4rem
</style>
