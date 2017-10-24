<template>
  <div class="hello">
    <section class="main">
    <section class="wrapper">
      <img height="150px" src="../assets/logo.svg" alt="react fest logo"/>
      <h1>ReactFest</h1>
      <h2>a one day festival of amazing React content</h2>

      <section class="susbscribe">
<form action="https://yld.us16.list-manage.com/subscribe/post?u=d159c019fc10dc08b3914ac05&amp;id=5a3093fa2a" method="post" id="mc-embedded-subscribe-form" name="mc-embedded-subscribe-form" class="validate" target="_blank" v-on:submit="onSubmit">
    <div id="fo">
      <h3>Subscribe to hear the latest ReactFest news</h3>
        <div class="fields">
          <input type="email" value="" placeholder="Your email" name="EMAIL" required class="email" id="mce-EMAIL">
          <div id="mce-responses" class="clear">
          <div class="response" style="display:none"></div>
          <div class="response" style="display:none"></div>
          </div>
              <div style="position: absolute; left: -5000px;" aria-hidden="true">
            <input type="text" name="b_d159c019fc10dc08b3914ac05_5a3093fa2a" tabindex="-1" value="">
            </div>
              <button type="submit" name="subscribe" class="submit" v-bind:class="{ submitted }">Subscribe</button>
              </div>
          </div>
</form>

      </section>
     </section>
    </section>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      submitted: false
    }
  },
  methods: {
    onSubmit: function () {
      this.submitted = true
    }
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

h1 {
  font-weight: bold;
  line-height: 57px;
  font-size: 100px;
  transition: all 200ms ease;

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

h3 {
  font-family: 'Roboto', sans-serif;
  font-weight: 500;
  line-height: 30px;
  font-size: 18px;
}

.email {
  width: 69%;
  height: 60px;
  background: #FFFFFF;
  border: none;
  box-sizing: border-box;
  box-shadow: 0px 2px 2px rgba(0, 0, 0, 0.05);
  padding: 10px;
  margin-right: 6px;
  color: #4A4A4A;
  border-radius: 0;

  &::-webkit-input-placeholder { /* Chrome/Opera/Safari */
    color: #9B9B9B;
  }
  &::-moz-placeholder { /* Firefox 19+ */
    color: #9B9B9B;
  }
  &:-ms-input-placeholder { /* IE 10+ */
    color: #9B9B9B;
  }
}

.submit {
  width: 30%;
  height: 60px;
  background: #37B75D;
  box-shadow: 0px 2px 2px rgba(0, 0, 0, 0.05);
  outline: none;
  color: #fff;
  border: none;
  font-family: 'Roboto', sans-serif;
  font-weight: bold;
  font-size: 16px;
  text-align: center;
  letter-spacing: 0.363636px;
  text-transform: uppercase;
  transition: all 200ms ease;
  cursor: pointer;

  color: #FFFFFF;

  &.submitted {
    width: 100%;
    position: absolute;
    text-indent: -9999999px;
    pointer-events: none;
    outline: none;

    &:before {
      content: 'Thank you for subscribing';
      position: absolute;
      width: 100%;
      height: 100%;
      left: 0;
      text-indent: 0;
    }
  }

  &:hover {
    background: #3dab5e;
  }
}

.fields {
  display: inline-flex;
  width: 100%;
  justify-content: center;
  align-self: center;
  position: relative;

  @media only screen and (max-width: 600px) {
    flex-direction: column;

    .submit {
      width: 100%;
      margin-top: 20px;
    }

    .email {
      width: 100%;
    }

  }
}

.hello {height: 100%; width: 100%;}
</style>
