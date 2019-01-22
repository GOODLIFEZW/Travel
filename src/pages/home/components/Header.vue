<template>
    <div class="header">
        <div class="header-left">
            <div class="iconfont back-icon">&#xe624;</div>
        </div>
        <div class="header-input">
            <span class="iconfont">&#xe632;</span>
            输入城市/景点/游玩主题
        </div>
        <router-link to='/city'>
            <div class="header-right">
                {{this.doubleCities}}
                <span class="iconfont">&#xe6aa;</span>
            </div>
        </router-link>
    </div>
</template>

<script>
import { mapState, mapGetters } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city']),
    ...mapGetters(['doubleCities'])
  }
}
</script>

<style lang="stylus" scoped>
    @import '~styles/varibles.styl'
    .header
        display flex
        line-height $headerHeight
        background $bgColor
        color #fff
        .header-left
            width .64rem
            .back-icon
                text-align center
                font-size .4rem
        .header-input
            flex 1
            background #fff
            margin-top .12rem
            margin-left .2rem
            height .64rem
            line-height .64rem
            border-radius .1rem
            color #ccc
            padding-left .2rem
        .header-right
            min-width 1.04rem
            padding 0 .1rem
            text-align center
            color #fff
</style>
