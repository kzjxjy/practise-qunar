<template>
    <div class="header">
        <div class="header-left">
            <div class="iconfont back-icon">&#xe624;</div>
        </div>
        <div class="header-input">
            <span class="iconfont">&#xe632;</span>
            输入城市/景点/游玩主题
        </div>
        <router-link to='/city' >
            <div class="header-right">
                {{this.city}}
                <span class="iconfont arrow-icon">&#xe600;</span>
            </div>
        </router-link>
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
@import '~styles/varibles.styl'
.header
    display: flex
    line-height: $headerHeight
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
        margin-top: .12rem
        margin-left: .2rem
        background: #fff
        border-radius: .1rem
        color: #ccc
        line-height: .64rem
        height: .64rem
        padding-left: .1rem
    .header-right
        width 1.24rem
        float: right
        text-align: center
        color: white
        .arrow-icon
            margin-left: -.04rem
            font-size: .2rem
</style>
