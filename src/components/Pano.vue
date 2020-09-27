<template>
  <div>
    <div id="viewer"></div>

  </div>
</template>
<script>
import { Viewer } from 'photo-sphere-viewer';
import 'photo-sphere-viewer/dist/photo-sphere-viewer.css'
export default {
  name: 'pano',
  data() {
    return {

    }
  },
  mounted() {
    this.initPhotoSphere()
  },
  methods: {
    initPhotoSphere() {
      new Viewer({
        container: document.querySelector('#viewer'),
        panorama: '0.jpg'
      });
    }
  }
}
</script>
<style lang="scss">
#viewer {
  margin: 0 auto;
  width: 100vh;
  height: 50vh;
}
</style>