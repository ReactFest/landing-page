<template>
  <main>
    <BlurredImage
      src="https://file-imaqlsttvx.now.sh/"
      small-src="https://file-bsyvngpoyb.now.sh/"
    ></BlurredImage>
    <Main/>
  </main>
</template>

<script>
import Main from './components/Main'
import BlurredImage from './components/BlurredImage'

export default {
  name: 'app',
  components: {
    Main,
    BlurredImage
  }
}
</script>

<style lang="scss">
@import '~normalize.css';
@import './assets/swedenSans/stylesheet.css';
@import url('https://fonts.googleapis.com/css?family=Roboto:500,900');

body,
html {
  margin: 0;
  height: 100%;
  width: 100%;

  @media only screen and (max-width: 600px) {
    min-height: 100%;
  }

  * {
    box-sizing: border-box;
  }
}

main {
  font-family: 'Sweden Sans', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #fff;
  text-align: center;
  height: 100%;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
</style>
