<template>
  <img :src="imageSrc" v-bind:class="{ loaded }"></img>
</template>

<script>
export default {
  name: 'BlurredImage',
  props: [
    'src',
    'smallSrc'
  ],
  data: function () {
    return {
      imageSrc: this.smallSrc,
      loaded: false
    }
  },
  mounted: function () {
    var img, that
    img = new Image()
    that = this
    img.onload = () => {
      that.imageSrc = that.src
      this.loaded = true
    }
    img.src = this.src
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

img {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translateX(-50%) translateY(-50%);
  height: 100vmax;
  filter: blur(10px);
  transition: all 200ms ease;
  z-index: -1;

  &.loaded {
      filter: blur(0);
  }

}
</style>
