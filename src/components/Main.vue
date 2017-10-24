<template>
  <section class="main">
    <section class="wrapper">
      <img height="150px" src="../assets/logo.svg" alt="react fest logo"/>
      <Headings />
      <Form />
    </section>
  </section>
</template>

<script>
import Form from './Form'
import Headings from './Headings'
export default {
  name: 'main',
  components: {
    Form,
    Headings
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.main {
  background: rgba(20, 33, 27, 0.6);;
  width: 100%;
  padding: 40px 0;
  min-height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;

  & .wrapper {
    max-width: 90%;
  }
}
</style>
