<template>
  <div id="app">
    <Marquee content="这里有六个字" speed="middle"></Marquee>
    <div class="tip">
      <Marquee content="这里有七个字啊" speed="middle"></Marquee>
    </div>
  </div>
</template>

<script>
import Marquee from './Marquee'
export default {
  name: 'App',
  components: {
    Marquee
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 60px auto 0;
  width: 100px;
  height: 40px;
  line-height: 40px;
  border: 1px solid #000;
}

</style>
