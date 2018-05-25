<template>
  <div id="join">
    <div class="join-header">
      <span class="join-title">入驻权大师 服务更简单</span>
      <a class="join-button" title="代理机构入驻权大师">立即入驻</a>
    </div>
    <div class="join-agent">
      <div class="join-agent-cont-wrapper">
        <div class="join-agent-cont">
          <div class="join-agent-cont-title">
            <span class="title-text">代理人推荐</span>
          </div>
          <ul class="join-agent-cont-list">
            <li class="list-item">
                <div class="agentphoto"></div>
                <div class="row-1"><span class="name">张 三</span><i class="cert">已认证</i></div>
                <div class="row-2">擅长：商标业务</div>
            </li>
            <li class="list-item">
                <div class="agentphoto"></div>
                <div class="row-1"><span class="name">李 四</span><i class="cert">已认证</i></div>
                <div class="row-2">擅长：商标业务</div>
            </li>
            <li class="list-item">
                <div class="agentphoto"></div>
                <div class="row-1"><span class="name">王 五</span><i class="cert">已认证</i></div>
                <div class="row-2">擅长：商标业务</div>
            </li>
            <li class="list-item">
                <div class="agentphoto"></div>
                <div class="row-1"><span class="name">赵 六</span><i class="cert">已认证</i></div>
                <div class="row-2">擅长：专利业务</div>
            </li>
            <li class="list-item">
                <div class="agentphoto"></div>
                <div class="row-1"><span class="name">徐 七</span><i class="cert">已认证</i></div>
                <div class="row-2">擅长：商标业务</div>
            </li>
          </ul>
        </div>
      </div>
    </div>
    <div class="join-header"></div>
  </div>
</template>

<script>
  export default {
    name: 'HomeJoin',
  }
</script>

<style>
  #join {
    margin-top: 160px;
    background: #e7f8ff;
    height: 440px;
    padding-bottom: 60px;
  }

  .join-header {
    height: 150px;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .join-header .join-title {
    color: #333;
    font-size: 32px;
    font-weight: bold;
  }

  .join-header .join-button {
    display: inline-block;
    height: 32px;
    line-height: 32px;
    padding: 0 25px;
    color: #f08b2f;
    font-size: 16px;
    border: solid 2px #f08b2f;
    border-radius: 20px;
    vertical-align: top;
    margin: 0 0 0 45px;
  }

  .join-agent-cont-wrapper {
    width: 100%;
    background: white;
  }

  .join-agent-cont {
    width: 1200px;
    margin: 0 auto;
    padding: 20px 0;
  }

  .join-agent-cont::after {
    clear:both;
    content: '';
    display: block;
  }

  .join-agent-cont-title {
    font-size: 18px;
    color: #222;
    border-left: 3px solid #f08b2f;
    border-radius: 1px;
    margin: 3px 8px 0 0;
  }

  .join-agent-cont-title .title-text {
    padding-left: 6px;
  }

  .join-agent-cont-list {
    display: flex;
    justify-content: center;
  }

  .join-agent-cont-list .list-item {
    float: left;
    width: 200px;
    padding: 15px 0px;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .join-agent-cont-list .list-item .row-1 {
    margin-top: 15px;
    display: flex;
    justify-content: center;
  }

  .join-agent-cont-list .list-item .row-1 .name {
    font-size: 18px;
    color: #333;
    display: flex;
    align-items: center;
  }
  .join-agent-cont-list .list-item .row-1 .cert {
    height: 18px;
    line-height: 18px;
    padding: 1px 6px;
    font-size: 12px;
    background-color: #3fb34f;
    color: #fff;
    border-radius: 2px;
    margin-left: 5px;
  }

  .join-agent-cont-list .list-item .row-2 {
    margin-top: 10px;
    font-size: 12px;
    color: #666;
  }

  .join-agent-cont .agentphoto {
    width: 120px;
    height: 120px;
    border-radius: 50%;
    background: #e7e4e4;
  }
</style>
