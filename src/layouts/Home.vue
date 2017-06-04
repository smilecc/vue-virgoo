<template>
  <div class="view-box">
    <img src="http://7xjvah.com1.z0.glb.clouddn.com/ds3_bg_home_character.png" class="character" :style="{ transform: characterTransform }">
    <particles></particles>
    <section class="news">
      <span class="title">最新消息</span>
      <div class="list">
        <div class="item">
          <a href="http://www.bilibili.com/video/av6619281/" target="_blank">黑暗之魂3 速通教学part3 完结篇</a>
          <small>2016.10.10</small>
        </div>
        <div class="item">
          <a href="http://www.bilibili.com/video/av6601368/" target="_blank">女神异闻录5 part9 全中文翻译</a>
          <small>2016.10.08</small>
        </div>
        <div class="item">
          <a href="http://www.bilibili.com/video/av6567829/" target="_blank">黑暗之魂3 速通教学P2 爵爵子配音版</a>
          <small>2016.10.06</small>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import Particles from '@/components/particles'
export default {
  components: {
    Particles,
    mixins:[
      require("vue-mixins/onMouseMove")
    ]
  },
  data () {
    return {
      characterTransform: 'translate3d(0px, 0px, 0px)'
    }
  },
  created () {
    document.onmousemove = (event) => {
      let percent = (event.clientX - window.innerWidth / 2) / window.innerWidth
      let position = (50 * percent)
      this.characterTransform =  'translate3d(' + position + 'px, 0px, 0px)'
    }
  },
  destory () {
    document.onmousemove = null
  }
}
</script>

<style lang="less">
.character {
  position: relative;
  display: block;
  left: 0px;
  top: 0px;
  bottom: 0;
  z-index: 1;
  height: 100%;
  transform-style: preserve-3d;
  backface-visibility: hidden;
}
.news {
  position: fixed;
  z-index: 10;
  right: 0;
  top: 0;
  padding: 25px;
  color: #FFF;
  margin: 20px;

  .title {
    position: relative;
    padding: 0 6px;
    width: auto;
    font-size: 13px;
    
    &:after, &:before {
      content: "";
      display: block;
      width: 100%;
      height: 1px;
      background: url(/static/line_white.png) center center no-repeat;
      background-size: 100% 1px;
      position: absolute;
      left: 0;
      opacity: 0.7;
      box-shadow: 0px 2px 1px 0 rgba(0, 0, 0, 0.75);
    }
    &:after {
      bottom: -6px;
    }
    &:before {
      top: -9px;
    }
  }
  .list {
    margin-top: 18px;
    font-size: 16px;
    font-family: UniversCom59UltraCondensed;
    .item {
      margin-bottom: 5px;
      small {
        font-size: 12px;
        color: #ccc;
      }
    }
    .item a {
      color: #fff;
      text-decoration: none;
      transition: all .2s;
      &:hover {
        color: #ccc;
      }
    }
  }
}
</style>
