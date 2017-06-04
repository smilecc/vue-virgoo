<template>
  <div id="app">
    <navbar></navbar>
    <router-view></router-view>
  </div>
</template>

<script>
import Navbar from '@/components/navbar'
export default {
  components: {
    Navbar
  },
  name: 'app'
}
</script>

<style>
@import '/static/font/UniversCom-59UltraCondensed/style.css';
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
}
html, body, #app {
  width: 100%;
  height: 100%;
}

* {
  margin: 0;
  padding: 0;
}
.view-box {
  width: calc(100% - 296px);
  height: 100%;
  position: absolute;
  top: 0;
  right: 0;
  background-image: url(http://7xjvah.com1.z0.glb.clouddn.com/ds3_bg_home.jpg);
  background-repeat: round;
}
</style>
