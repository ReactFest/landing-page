<template>
  <div>
      <h1>ReactFest</h1>
      <h3>London , 2 March 2018</h3>
      <h2>a one day festival of amazing React content</h2>
  </div>
</template>

<script>
export default {
  name: 'headings'
}
</script>

<style lang="scss" scoped>
h1 {
  font-weight: bold;
  line-height: 57px;
  font-size: 100px;
  transition: all 200ms ease;
  margin-bottom: 0;

  +  h3 {
    margin-top: 0;
    font-size: 24px;
  }

  @media only screen and (max-width: 600px) {
    font-size: 60px;
  }
}

h2 {
  font-family: 'Roboto', sans-serif;
  font-weight: 900;
  line-height: 50px;
  font-size: 40px;

  @media only screen and (max-width: 600px) {
    font-size: 30px;
  }
}
</style>

