<template>
  <canvas id="particles"></canvas>
</template>

<script>
const config = {
  num       : 200, // 数量
  size      : {
    minSize: 1, // 最小尺寸
    maxSize: 2 // 最大尺寸
  },
  zone      : {
      x: [0.01, 0.99],
      y: [0.01, 0.99]
  },
  speed     : {
    x : [-10, 2], // x轴速度区间
    y : [-1, 1], // y轴速度区间
    ax: [-0.01, 0.01], // x轴加速度区间
    ay: [-0.01, 0.01] // y轴加速度区间
  },
  time      : {
    fadeIn : 500, // 生成时间
    fadeOut: 4000 // 消逝时间
  },
  atmosphere: [ // 色彩氛围，在指定颜色区间中随机生成颜色效果真是棒极了！
    {
      start:{
        r: 237,
        g: 118,
        b: 54,
        a: 1
      },
      end:{
        r: 217,
        g: 88,
        b: 19,
        a: 1
      }
    }
  ],
  background: "rgba(0, 0, 0, 0)",
  follow    : false,
  active    : 0, // 鼠标随动程度
  blur      : true // 模糊效果……存在性能问题但不舍得抛弃_(:3」∠)_
}

export default {
  name: 'particles',
  mounted () {
    var ml = mapleParticles(window.document.getElementById("particles"), config)
  }
}
</script>

<style scoped>
#particles {
  width : 100%;
  height : 100%;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 2;
  -webkit-transform: scale(2);
  transform: scale(2);
}
</style>
