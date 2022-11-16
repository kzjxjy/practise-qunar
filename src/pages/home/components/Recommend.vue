<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
        <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
                <img :src="item.imgUrl" class="item-img">
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
      recommendList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/2005/9e/9e643f96c84b5c2ea3.water.jpg_200x200_2a3eef5b.jpg',
        title: '上海欢乐谷',
        desc: '上海市松江区佘山镇林湖路888号'
      }, {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/2005/9e/9e643f96c84b5c2ea3.water.jpg_200x200_2a3eef5b.jpg',
        title: '上海欢乐谷',
        desc: '上海市松江区佘山镇林湖路888号'
      }, {
        id: '0003',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/2005/9e/9e643f96c84b5c2ea3.water.jpg_200x200_2a3eef5b.jpg',
        title: '上海欢乐谷',
        desc: '上海市松江区佘山镇林湖路888号'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl';
.title
  line-height: .8rem
  background: #eee
  text-indent: .2rem
  margin-top: .2rem
.item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
        width: 1.7rem
        height: 1.7rem
        padding: .1rem
    .item-info
        flex: 1 //自动撑开屏幕宽度
        padding: .1rem
        min-width: 0
        .item-title
            line-height: .54rem
            font-size: .32rem
            ellipsis()
        .item-desc
            padding-top: .06rem
            line-height: .4rem
            color: #ccc
            ellipsis()
        .item-button
            line-height: .5rem
            margin-top: .2rem
            background: #ff9300
            padding: 0 .2rem
            border-radius: .06rem
            color: #fff
</style>
