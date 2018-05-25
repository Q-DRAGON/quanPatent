<template>
  <div id="info">
    <div class="info-news">
        <h3 class="info-news-title">权资讯</h3>
        <dl class="info-news-list">
            <dt>
                <span class="time-day">11</span>
                <span class="time-month">2018-05</span>
            </dt>
            <dd>
                <h3 class="list-title">2018年4月各类别商标申请量排名丨权大师发布</h3>
                <p class="list-cont">权大师发布2018年4月份各类别商标申请量排名榜单，数据申请时间范围为2018年4月1日~4月30日，欢迎查看。</p>
            </dd>
        </dl>
        <dl class="info-news-list">
            <dt>
                <span class="time-day">11</span>
                <span class="time-month">2018-05</span>
            </dt>
            <dd>
                <h3 class="list-title">2018年4月各类别商标申请量排名丨权大师发布</h3>
                <p class="list-cont">权大师发布2018年4月份各类别商标申请量排名榜单，数据申请时间范围为2018年4月1日~4月30日，欢迎查看。</p>
            </dd>
        </dl>
        <dl class="info-news-list">
            <dt>
                <span class="time-day">11</span>
                <span class="time-month">2018-05</span>
            </dt>
            <dd>
                <h3 class="list-title">2018年4月各类别商标申请量排名丨权大师发布</h3>
                <p class="list-cont">权大师发布2018年4月份各类别商标申请量排名榜单，数据申请时间范围为2018年4月1日~4月30日，欢迎查看。</p>
            </dd>
        </dl>
    </div>
    <div class="info-know">
      <h3 class="info-know-title">权知道</h3>
      <div class="info-know-body">
        <dl class="info-know-list" v-for="(item, index) of knowList">
            <dt>
               <span class="list-icon">商标</span>
            </dt>
            <dd>
              <span class="list-title">{{item.title}}</span>
                <div class="list-text">
                  <span class="list-cont">
                    {{item.cont}}
                  </span>
                </div>
            </dd>
        </dl>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'HomeInfo',
    data() {
      return {
        knowList: [
          {
            title: '申请注册后的商标,后期字体或颜色发生变化还受保护?',
            cont: '您好，原则上商标怎么申请就应该怎么使用。如果申请时提交的是黑白图标，则使用时可以使用任意颜色的图标',
          },
          {
            title: '商标被驳回怎么办？',
            cont: '您好，商标驳回分为两种，一种是全部驳回，一种是部分驳回。遇到商标驳回时，您可以根据具体的驳回项目、驳',
          },
          {
            title: '怎么注册商标？',
            cont: '您可以先想好一个商标名称，然后进入保姆式商标注册，搜索代理人：王淑勤，我可以帮您查询并评估商标是否能',
          },
          {
            title: '我可以申请注册“***”商标吗？',
            cont: '您可以在权大师的商标搜索中输入需要申请的商标名称查询，如果没有人在相关类别上申请相同的商标，那么就可',
          },
        ]
      }
    }
  }
</script>

<style>
  #info {
    width: 1200px;
    margin: 0 auto;
    padding: 32px 0 35px;
    padding-top: 50px;
  }

  #info::after {
    clear: both;
    display: block;
    content: '';
  }

  .info-news {
    width: 715px;
    height: 400px;
    float: left;
  }

  .info-news-title,.info-know-title {
    font-size: 26px;
    font-weight: 500;
    margin-bottom: 30px;
  }

  .info-news-list {
    padding: 18px 0 25px;
    border-bottom: dotted 1px #bfbfbf;
    display: flex;
  }

  .info-news-list dt {
    width: 92px;
    height: 78px;
    text-align: center;
    color: #dbdbdb;
  }

  .info-news-list dt .time-day {
    display: block;
    font-size: 60px;
    line-height: 55px;
  }

  .info-news-list dt .time-month {
    display: block;
    font-size: 18px;
    line-height: 28px;
  }

  .info-news-list dd {
    margin-left: 20px;
  }

  .info-news-list dd .list-title {
    font-size: 20px;
    color: #555;
    margin-bottom: 10px;
  }

  .info-news-list dd .list-cont {
    font-size: 14px;
    color: #999;
    line-height: 26px;
  }

  .info-know {
    width: 435px;
    height: 400px;
    float: right;
  }

  .info-know-body {
    height: 350px;
    overflow-y: auto;
  }

  .info-know-list {
    display: flex;
    margin-bottom: 26px;

  }

  .info-know-list dt .list-icon {
    display: inline-block;
    width: 35px;
    height: 20px;
    line-height: 20px;
    font-size: 12px;
    background-color: #f08b2f;
    color: #fff;
    border-radius: 3px;
    text-align: center;
    margin-right: 10px;
  }

  .info-know-list dd  {
    width: 345px;
  }

  .info-know-list dd .list-text {
    margin-top: 10px;
    background: #f5f5f5;
    padding: 10px;
  }

  .info-know-list dd .list-text .list-cont {
    font-size: 12px;
    color: #666;
    line-height: 22px;
  }

  /* 更改权知道的滚动条样式 */
  .info-know-body::-webkit-scrollbar {
    width: 7px;
  }

  .info-know-body::-webkit-scrollbar-thumb {
      background-color: #f08b2f;
      border-radius: 8px;
  }

  .info-know-body::-webkit-scrollbar-track-piece {
    background-color: #eee;
  }
</style>
