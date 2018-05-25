<template>
  <div class="home">
    <home-header></home-header>
    <home-drop></home-drop>
    <home-banner></home-banner>
    <home-hot-tools></home-hot-tools>
    <home-join></home-join>
    <home-info></home-info>
    <home-rating></home-rating>
  </div>
</template>

<script>
import HomeHeader from './component/header.vue'
import HomeDrop from './component/drop.vue'
import HomeBanner from './component/banner.vue'
import HomeHotTools from './component/hottools.vue'
import HomeJoin from './component/join.vue'
import HomeInfo from './component/info.vue'
import HomeRating from './component/rating.vue'

export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeDrop,
    HomeBanner,
    HomeHotTools,
    HomeJoin,
    HomeInfo,
    HomeRating
  }
}
</script>

<style>
</style>
