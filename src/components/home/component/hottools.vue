<template>
  <div id="HotTools">
    <div class="title">
      <span class="title-text">热门工具</span>
    </div>
    <div class="cont-wrapper">
      <div class="cont-left">
        <div
        class="cont-left-icon-wrapper"
        id="login"
        @mouseenter="handleMouseEnterForIcon">
          <div class="cont-left-icon" :class="{active: colorActive === 'login'}"></div>
          <span>智能商标注册</span>
        </div>
        <div
        class="cont-left-icon-wrapper"
        id="monitor"
        @mouseenter="handleMouseEnterForIcon">
          <div class="cont-left-icon" :class="{active: colorActive === 'monitor'}"></div>
          <span>智能监控</span>
        </div>
        <div
        class="cont-left-icon-wrapper"
        id="moretools"
        @mouseenter="handleMouseEnterForIcon">
          <div class="cont-left-icon" :class="{active: colorActive === 'moretools'}"></div>
          <span>更多工具</span>
        </div>
      </div>
      <div class="cont-right">
        <img
        src="https://www.quandashi.com/qdshome/images/bg-tools-sbjk.jpg"
        v-show="iconActive === 'login'"
        alt="智能商标注册">
        <img
        src="https://www.quandashi.com/qdshome/images/bg-tools-znzc.jpg"
        v-show="iconActive === 'monitor'"
         alt="商标监控">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHotTools',
  data() {
    return {
      iconActive: 'login',
      colorActive: 'login',
    }
  },
  methods: {
    handleMouseEnterForIcon() {
      if(event.target.id == 'moretools') {
        this.colorActive = event.target.id
      } else {
        this.colorActive = event.target.id
        this.iconActive = event.target.id
      }
    }
  }
}
</script>

<style scoped>
  #HotTools {
    width: 1200px;
    margin: 0 auto;
    margin-top: 60px;
  }

  .title {
    font-size: 18px;
    color: #222;
    border-left: 3px solid #f08b2f;
    border-radius: 1px;
    margin: 3px 8px 0 0;
  }

  .title .title-text {
    padding-left: 6px;
  }

  .cont-left {
    float: left;
    width: 120px;
    padding: 0 0 0 43px;
    margin-top: 40px;
    border-right: solid 2px #f3f3f3;
  }

  .cont-left-icon-wrapper {
    width: 90px;
    white-space:nowrap;
    text-align: center;
    margin-top: 20px;
    margin-bottom: 20px;
  }

  .cont-left-icon-wrapper + .cont-left-icon-wrapper {
    margin-top: 40px;
  }

  .cont-left-icon {
    background: #f08b2f;
    border-radius: 50%;
    width: 70px;
    height: 70px;
    margin: 10px auto;
  }

  .active {
    background: lightblue;
    transition: all .3s linear;
  }

  .cont-wrapper::after {
      clear:both;
      content: '';
      display: block;
  }

  .cont-wrapper {
    width: 1200px;
  }

  .cont-right {
    float: left;
    width: 900px;
    height: 500px;
    margin: 0 0 0 90px;
  }
</style>
