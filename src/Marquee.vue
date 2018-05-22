<template>
  <div class="wrap" ref="out">
    <div :class="['content', run?speed: '']">
      <span class="line" v-html="content" ref="in"></span>
      <span v-if="run" class="line" v-html="content"></span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'marquee',
  computed: {


  },
  props: {
    content: {
      default: '暂无内容',
      type: String
    },
    speed: {
      default: 'quick',
      type: String
    }
  },
  data () {
    return {
      run: false
    }
  },
  mounted() {
    this.$nextTick(()=> {
        this.run = this.$refs.in.clientWidth > this.$refs.out.clientWidth;
    })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.wrap {
  overflow: hidden;
}

.line {
  display: inline-block;
  margin-right: 20px;
}

.content {
  white-space: nowrap;
  display: inline-block;
  margin: 0;
}

.quick{
  -webkit-animation: marquee 5s linear infinite;
  animation: marquee 5s linear infinite;
}
.middle{
  -webkit-animation: marquee 8s linear infinite;
  animation: marquee 8s linear infinite;
}
.slow{
  -webkit-animation: marquee 25s linear infinite;
  animation: marquee 25s linear infinite;
}

@-webkit-keyframes marquee {
  0%  { -webkit-transform: translate3d(0,0,0); }
  100% { -webkit-transform: translate3d(-50%,0,0); }
}
@keyframes marquee {
  0%  { transform: translateX(0); }
  100% { transform: translateX(-50%);}
}
</style>
