<template>
  <div>
      <h1>ReactFest</h1>
      <h2>A One Day Festival of Amazing React Content</h2>
      <h3>Single track. 200 developers. Non-profit. By the community for the community.</h3>
      <h2 class="date">9th March 2018, London</h2>
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
  font-family: 'Sweden Sans', sans-serif;

  @media only screen and (max-width: 600px) {
    font-size: 60px;
  }
}

.date {
  margin-top: 80px;
}

h2 {
  font-family: 'Roboto', sans-serif;
  font-weight: 900;
  line-height: 50px;
  font-size: 40px;
  margin-bottom: 0;

  +  h3 {
    margin-top: 10px;
    font-size: 24px;
  }

  @media only screen and (max-width: 600px) {
    font-size: 30px;
  }
}
</style>

