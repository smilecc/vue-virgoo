<template>
  <section>
    <div class="title">VIRGOO TEAM</div>
    <div class="index">
      <div class="item active">
        <span class="numb">I</span>
        <span class="text">首页</span>
      </div>
      <div class="item">
        <span class="numb">II</span>
        <span class="text">动态</span>
      </div>
      <div class="item">
        <span class="numb">III</span>
        <span class="text">视频</span>
      </div>
      <div class="item">
        <span class="numb">IV</span>
        <span class="text">支持我们</span>
      </div>
    </div>
    <div class="copyright">
      <p>VirgooTeam 2017.</p>
      <p>Design by Can.</p>
    </div>
  </section>
</template>

<script>
export default {
  name: 'navbar'
}
</script>

<style scoped lang="less">
@import '/static/font/optimusprincepssemibold/style.css';
@import '/static/font/TrajanPro/style.css';
section {
  width: 296px;
  height: 100%;
  background: url(/static/nav.jpg) left top no-repeat #0c0b09;
  position: fixed;
  top: 0;
  z-index: 10;
  background-size: auto 1024px;
  color: #fff;
  border-right: solid 2px #1a1a1a;
}
.title {
  position: relative;
  font-family: optimusprincepssemiboldRg;
  font-size: 30px;
  text-align: center;
  margin-top: 50px;
  color: #f1f1f1;
  letter-spacing: 2px;
  width: 260px;
  margin: 50px auto 0;
  &:before {
    content: "";
    display: block;
    width: 100%;
    height: 1px;
    background: url(/static/line_white.png) center center no-repeat;
    background-size: 100% 1px;
    position: absolute;
    left: 0;
    top: 15px;
    opacity: 0.4;
    box-shadow: 0px 2px 1px 0 rgba(0, 0, 0, 0.75);
  }
}
.index {
  width: 170px;
  margin: 50px auto 23px;
  .item {
    margin-bottom: 3px;
    width: 100%;
    padding-left: 53px;
    position: relative;
    font-size: 20px;
    color: rgb(156, 156, 156);
    cursor: pointer;
    
    .numb {
      font-family: TrajanPro;
      width: 20px;
      text-align: center;
      position: absolute;
      left: 0;
      height: 34px;
      top: -1px;
      z-index: 0;
      font-size: 14px;
      line-height: 34px;
      vertical-align: middle;
      text-align: center;
    }
    .text {
      font-family: UniversCom59UltraCondensed;
    }
    .numb, .text {
      transition: all 0.3s;
    }
  }

  .item.active, .item:hover {
    .numb {
      color: #fff;
    }
    .text {
      color: rgb(189, 153, 77);
    }
  }
}
.copyright {
  font-family: TrajanPro;
  font-size: 13px;
  position: absolute;
  bottom: 0;
  padding: 30px;
  color: #444;
}
</style>
