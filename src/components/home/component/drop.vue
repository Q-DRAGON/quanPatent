<template>
  <div class="drop-wrapper" @mouseleave="handleMouseLeave">
    <div class="drop-body">
      <div
      class="main-drop-title" @mouseenter="handleMouseEnterNone">
        <span class="title-text">全部业务</span>
      </div>
      <div
      class="drop-title"
      id="brand"
      :class="{dropActive: isShowData === 'brand'}"
      @mouseenter="handleMouseEnter">
        <span class="title-text">商标业务</span>
      </div>
      <div
      class="drop-title"
      id="patent"
      :class="{dropActive: isShowData === 'patent'}"
      @mouseenter="handleMouseEnter">
        <span class="title-text">专利业务</span>
      </div>
      <div
      class="drop-title"
      id="copyright"
      :class="{dropActive: isShowData === 'copyright'}"
      @mouseenter="handleMouseEnter">
        <span class="title-text">版权业务</span>
      </div>
      <div
      class="drop-title"
      id="startup"
      :class="{dropActive: isShowData === 'startup'}"
      @mouseenter="handleMouseEnter">
        <span class="title-text">创业业务</span>
      </div>
      <div class="drop-none" @mouseenter="handleMouseEnterNone">

      </div>
    </div>
    <div class="drop-menu" v-show="dropMenuShow" @mouseleave="handleMouseLeave">
      <div v-for="(value, key) in menuData" v-show="key == isShowData">
        <dl v-for="(key, value) of value">
          <dt>
            <a href="#">{{key.dt}}</a>
          </dt>
          <dd>
            <a href="#" v-for="(value,index) of key.dd">{{value}}</a>
          </dd>
        </dl>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeDrop',
  data() {
    return {
      dropMenuShow: false,
      isShowData: '',
      menuData: {
        'brand': [
          {
            dt: '查询是否可以注册',
            dd: [
              '免费商标查询',
              '国内商标查询',
            ]
          },{
            dt: '快速办理商标注册',
            dd: [
              '保姆注册',
              '智能注册',
            ]
          },
        ],
        'patent': [
          {
            dt: '查询是否可申请专利',
            dd: [
              '专利检索报告',
            ]
          },{
            dt: '设计方法创新',
            dd: [
              '发明专利-技术型',
              '发明专利-防御型',
            ]
          },
        ]
      }
    }
  },
  methods: {
    handleMouseEnter(event) {
      console.log('event', event.target.id)
      this.dropMenuShow = true
      this.isShowData = event.target.id
    },
    handleMouseLeave() {
      this.dropMenuShow = false
      this.isShowData = ''
    },
    handleMouseEnterNone() {
      this.dropMenuShow = false
      this.isShowData = ''
    }
  }
}
</script>

<style scoped>
  .drop-wrapper {
    width: 1200px;
    margin: auto;
    position: relative;
    z-index: 1000;
  }

  .drop-body {
    background-color: rgba(51, 51, 51, .8);
    width: 200px;
    position: absolute;
    margin: 0 auto;
    top: -38px;
    height: 536px;
  }

  .drop-none {
    height: 50%;
  }

  .drop-title {
    padding: 21px 22px 22px 48px;
    color: #fff;
    font-size: 15px;
    border-bottom: solid 1px grey;
  }

  .main-drop-title {
    height: 38px;
    line-height: 38px;
    background-color: rgba(51, 51, 51, 1);
    cursor: pointer;
    text-align: center;
    border: solid 1px #000;
    color: #fff;
    opacity: 1;
  }

  .drop-menu {
    position: absolute;
    top: 0px;
    left: 199px;
    width: 1000px;
    height: 394px;
    background-color: #fff;
    border: solid 1px #333;
    z-index: 1;
  }

  .drop-menu dl {
    display: flex;
    margin-left: 20px;
    width: 690px;
    border-bottom: 1px solid #ddd;
  }

  .drop-menu dt {
    float: left;
    position: relative;
    width: 140px;
    padding: 22px 16px;
  }

  .drop-menu dd {
    float: left;
    width: 515px;
    padding: 15px 10px;
  }

  .drop-menu dd a {
    font-size: 12px;
    color: #333;
    display: block;
    position: relative;
    float: left;
    margin: 6px 0px;
    padding: 1px 15px;
    border-left: 1px solid lightgrey;
  }

  .drop-menu dt a {
    font-size: 13px;
    color: #999;
  }

  .dropActive {
    background: white;
    color: black;
  }

</style>
