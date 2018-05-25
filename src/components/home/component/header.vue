<template>
  <div class="header">
    <div class="header-logo">
      <img src="../../../assets/logo.png" alt="" />
    </div>
    <div class="search">
      <div class='search-items'>
        <div
        class='search-item'
        id="brandForSearch"
        :class="{searchActive: isShowSearch === 'brandForSearch'}"
        @click="handleClickForSearch">商标</div>
        <div
        class='search-item'
        id="patentForSearch"
        :class="{searchActive: isShowSearch === 'patentForSearch'}"
        @click="handleClickForSearch">专利</div>
        <div
        class='search-item'
        id="enterpriseForSearch"
        :class="{searchActive: isShowSearch === 'enterpriseForSearch'}"
        @click="handleClickForSearch">企业</div>
      </div>
      <div class="search-input-wrapper">
        <input type="text" name="name" value="" class="search-input">
        <input type="submit" class="search-submit">
      </div>
    </div>
    <div class="topbar">
      <div class='topbar-item'>商标注册</div>
      <div class='topbar-item'>发明专利</div>
      <div class='topbar-item'>软件著作版权</div>
      <div class='topbar-item'>商标监控</div>
      <div class='topbar-item'>知识产权工具</div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'HomeHeader',
  data() {
    return {
      isShowSearch: 'brandForSearch',
    }
  },
  methods: {
    handleClickForSearch() {
      this.isShowSearch = event.target.id
      console.log('search = ', this.isShowSearch)
    }
  }
}
</script>

<style scoped>
  .header {
    width: 1200px;
    margin: auto;
  }

  .header-logo {
    width: 100px;
    display: inline-block;
    margin: 35px 0 0 30px;
  }

  .header-logo img {
    width: 100%;
  }

  .search {
    display: inline-block;
    margin: 35px 0 0 130px;
    font-size: 14px;
    vertical-align: top;
  }

  .search-input-wrapper {
    display: flex;
    width: 630px;
    border: 1px solid #f08b2f;
    height: 42px;
  }

  .search-input {
    flex: 1;
    height: 100%;
    border: 0;
    outline: none;
    padding: 0;
    padding-left: 10px;
    font-size: 16px;
  }

  .search-submit {
    width: 140px;
    height: 100%;
    border: 0;
    background-color: #f08b2f;
    cursor: pointer;
    color: white;
  }

  .search-items {
    display: block;
  }

  .search-items::after {
    display: block;
    content: '';
    clear: both;
  }

  .search-items .search-item {
    float: left;
    height: 27px;
    line-height: 29px;
    padding: 0 22px;
    cursor: pointer;
    background-color: #fff;
  }

  .topbar {
    margin-top: 20px;
    display: flex;
    justify-content: flex-end;
  }

  .topbar::after {
    display: block;
    content: '';
    clear: both;
  }

  .topbar .topbar-item {
    float: left;
    padding: 0 50px;
    height: 38px;
    line-height: 38px;
    color: #000;
    font-size: 17px;
  }

  .search-items .searchActive {
    color: #333;
    background-color: #f08b2f;
  }
</style>
