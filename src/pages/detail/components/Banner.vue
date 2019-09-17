<template>
  <div>
    <div class="banner"  @click="handleBannerClick">
      <img class="banner-img" src="http://img1.qunarzz.com/sight/p0/1804/1a/1a48cc20b0d6ed44a3.img.jpg_600x330_3f524da7.jpg" alt="img">
      <div class="banner-info">
        <div class="banner-title">神圣地宫大宝塔</div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe623;</span>
          66
        </div>
      </div>
    </div>
    <common-gallary :imgs='imgs' v-show="showGallary" @close="handleGallaryClose"></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: [
        'http://img1.qunarzz.com/sight/p0/1511/34/34170b200db08a5a90.img.jpg_r_800x800_313a5a50.jpg',
        'http://img1.qunarzz.com/sight/p0/1511/34/34170b200db08a5a90.img.jpg_r_800x800_313a5a50.jpg'
      ]
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  components: {
    CommonGallary
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    overflow: hidden
    position: relative
    height: 0
    padding-bottom: 55%
    .banner-img
      width: 100%
    .banner-info
      display: flex
      position: absolute
      left: 0
      right:0
      bottom: 0
      line-height: .6rem
      color: #fff
      background-image: linear-gradient(top, rgba(0,0,0,0), rgba(0,0,0,.8))
      .banner-title
        flex: 1
        font-size: .32rem
        padding: 0 .2rem
      .banner-number
        height: .32rem
        line-height: .32rem
        margin-top: .14rem
        padding: 0 .4rem
        border-radius: .2rem
        background: rgba(0, 0, 0, .8)
        font-size: .24rem
        .banner-icon
          font-size: .24rem
</style>
