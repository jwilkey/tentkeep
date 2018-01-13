<template>
  <div class="home">
    <div class="banner-wrapper flex-column flex-center align-center shadow-long">
      <div class="banner cover"></div>

      <div class="flex-one pad"></div>
      <div class="z1">
        <h1 class="text-center shadow-long z1 banner-label">TENTKEEP</h1>
      </div>
      <div class="flex-one pad z1">
        <p class="banner-label-alt small-pad rounded">SOFTWARE • WEB • GRAPHICS • SOUND</p>
      </div>
    </div>

    <div class="pad">
      <div class="text-center">
        <button @click="contactUs">Contact us. Let's make something. <i class="fas fa-arrow-alt-circle-right"></i></button>
      </div>

      <div class="cost-slogan text-center pad marginb">
        <p>Service options ranging from affordable to premium.</p>
        <p>Always honest. Always excellent.</p>
      </div>

      <div class="conditional-row">
        <div class="small-pad">
          <div class="theme-mid rounded shadow pad">
            <p class="callout alt text-center">SOFTWARE</p>
            <div class="icon-wrapper hi-bottom">
              <img class="icon" src="../../static/images/coding.svg" />
            </div>
            <div class="small-pad">
              <div class="text-center margint">
                <p>iOS &amp; Android apps</p>
                <p>Backend servers</p>
                <p>Full stack apps</p>
              </div>
            </div>
          </div>
        </div>

        <div class="small-pad">
          <div class="theme-mid rounded shadow pad">
            <p class="callout alt text-center">WEB</p>
            <div class="icon-wrapper hi-bottom">
              <img class="icon" src="../../static/images/internet.svg" />
            </div>
            <div class="small-pad">
              <div class="text-center margint">
                <p>Business websites</p>
                <p>Web stores</p>
                <p>Web apps</p>
              </div>
            </div>
          </div>
        </div>

        <div class="small-pad">
          <div class="theme-mid rounded shadow pad">
            <p class="callout alt text-center">GRAPHICS</p>
            <div class="icon-wrapper hi-bottom">
              <img class="icon" src="../../static/images/gallery.svg" />
            </div>
            <div class="small-pad">
              <div class="text-center margint">
                <p>Logos</p>
                <p>Infographics</p>
                <p>Marketing</p>
              </div>
            </div>
          </div>
        </div>

        <div class="small-pad">
          <div class="theme-mid rounded shadow pad">
            <p class="callout alt text-center">SOUND</p>
            <div class="icon-wrapper hi-bottom">
              <img class="icon" src="../../static/images/speaker.svg" />
            </div>
            <div class="small-pad">
              <div class="text-center margint">
                <p>Background music</p>
                <p>Game music &amp; FX</p>
                <p>Brand music</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'home',
  data () {
    return {
    }
  },
  methods: {
    contactUs () {
      this.$router.push('/contact')
    }
  }
}
</script>

<style lang="less" scoped>
.home {
  .banner-wrapper {
    position: relative;
    height: 250px;
    border-bottom: solid black 5px;
    .banner {
      margin: -5px;
      background-image: url('../../static/images/banner.jpeg');
      background-size: cover;
      background-position: center;
      filter: grayscale(80%) brightness(150%) blur(1px);
    }
    .banner-label {
      color: black;
      text-shadow: 0px 0px 15px white;
      background-color: rgba(255, 255, 255, 0.9);
    }
    .banner-label-alt {
      color: white;
      text-shadow: 0px 0px 5px black;
      // background-color: rgba(255, 255, 255, 0.9);
    }
    h1 {
      margin: 0;
      font-weight: lighter;
      letter-spacing: 1px;
      padding: 15px 30px;
    }
  }
  .cost-slogan {
    & > * {
      padding: 0 7px;
    }
  }
  .icon-wrapper {
    padding: 10% 20%;
    .icon {
      max-height: 90px;
      opacity: 0.7;
    }
  }
}
</style>
