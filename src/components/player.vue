<template>
  <div>
    <video id="videoElement" controls autoplay muted width="400px" height="800px"></video>
    <button @click="play">播放</button>
  </div>

</template>

<script>
import flvjs from 'flv.js'
export default {
  name: "player" ,
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      flvPlayer:null
    }
  },
  mounted() {
    if (flvjs.isSupported()) {
      var videoElement = document.getElementById('videoElement');
      this.flvPlayer = flvjs.createPlayer({
        type: 'flv',
        isLive: true,
        hasAudio: false,
        url: 'http://117.40.182.188:10800/flv/hls/stream_3.flv'
      });
      this.flvPlayer.attachMediaElement(videoElement);
      this.flvPlayer.load();
      this.flvPlayer.play();
    }
  },
  methods:{
    play () {
      this.flvPlayer.play();
    }
  }
  ,

}
</script>

<style scoped>

</style>