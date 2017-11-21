<template>
  <section class="subscribe-wrapper">
      <a href="https://t.co/bWzDRNZzQA"
        class="submit">
          <span>BECOME A SPEAKER</span>
      </a>
    <form action="https://yld.us16.list-manage.com/subscribe/post?u=d159c019fc10dc08b3914ac05&amp;id=5a3093fa2a" method="post" id="mc-embedded-subscribe-form" name="mc-embedded-subscribe-form" class="validate" target="_blank" v-on:submit="onSubmit">
      <h3>Subscribe to hear about the latest ReactFest news</h3>
        <div class="fields">
          <input type="email" value="" placeholder="Your email" name="EMAIL" required class="email" id="mce-EMAIL">
          <div id="mce-responses" class="clear">
          <div class="response" style="display:none"></div>
          <div class="response" style="display:none"></div>
          </div>
          <div style="position: absolute; left: -5000px;" aria-hidden="true">
            <input type="text"
              name="b_d159c019fc10dc08b3914ac05_5a3093fa2a"
              tabindex="-1"
              value="">
            </div>
              <button
                type="submit"
                name="subscribe"
                class="submit"
                v-bind:class="{ submitted }">
                  Subscribe
                </button>
          </div>
    </form>
    <div class="section">
      <ul>
        <li>
          <a href="mailto:hey@reactfest.com">
            <img src="../assets/email.svg"  width="40px">
          </a>
        </li>
        <li>
          <a href="https://github.com/ReactFest" target="_blank" rel="noopener">
            <img src="../assets/github.svg"  width="40px">
          </a>
        </li>
        <li>
          <a href="https://twitter.com/ReactFest/" target="_blank" rel="noopener">
            <img src="../assets/twitter.svg"  width="40px">
          </a>
        </li>
      </ul>
        <p>If you would like to sponsor please email at: <a href="mailto:hello@reactfest.com">hello@reactfest.com</a></p>
      </div>
</section>
</template>

<script>
export default {
  name: 'Form',
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

<style lang="scss" scoped>

  .section {
    position: relative;
    margin-top: 150px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100%;

  @media only screen and (max-width: 600px) {
    margin-top: 50px;
  }


    ul {
      display: flex;
      align-items: center;
      justify-content: center;
    }

    li {
      list-style: none;
      margin: 0 20px;
    }
  }

h3 {
  font-family: 'Roboto', sans-serif;
  font-weight: 500;
  line-height: 30px;
  font-size: 18px;
}

p {
  font-family: 'Roboto', sans-serif;
  font-weight: 500;
  font-size: 15px;
  display: block;
  width: 100%;

  a {
    color: #37B75D;
    text-decoration: none;

    &:hover {
      text-decoration: underline;
    }
  }
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
  font-family: 'Roboto', sans-serif;
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
  display: block;
  text-decoration: none;
  line-height: 60px;
  margin: auto;

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

a.submit {
  margin-bottom: 60px;
  background: #4A4A4A;
  color: #FFF;
  text-transform: uppercase;
  position: relative;
  transition: all 200ms ease;
  left: 5px;

  @media only screen and (max-width: 600px) {
    width: 100%;
  }

  &:active,
  &:hover {
    &:before {
      top: 1px;
      right: 1px;
    }

    &:after {
      top: 2px;
      right: 2px;
    }
  }


  span {
    z-index: 10;
    display: block;
    position: relative;
    background: #4A4A4A;
    color: #FFF;
    width: 100%;
    height: 100%;
  }

  &:before {
    position: absolute;
    content: '';
    width: 100%;
    height: 100%;
    background: #FFF;
    top: 5px;
    right: 5px;
    z-index: 2;
    transition: all 200ms ease;
  }

  &:after {
    position: absolute;
    content: '';
    width: 100%;
    height: 100%;
    background: #37B75D;
    top: 10px;
    right: 10px;
    z-index: 1;
    transition: all 200ms ease;
  }
}

@media only screen and (max-width: 600px) {
    flex-direction: column;

  .submit,
  a.submit{
    width: 100%;
    margin-top: 20px;
  }

  .email {
    width: 100%;
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

  .submit,
  a.submit{
    width: 100%;
    margin-top: 20px;
  }

  .email {
    width: 100%;
  }
  }
}

.subscribe-wrapper {
  margin-top: 40px;
  position: relative;
}
</style>
