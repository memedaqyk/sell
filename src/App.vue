<template>
  <div>
    <!--头部-->
    <myheader :poiInfo="poiInfo"></myheader>
    <!--导航-->
    <mynav></mynav>
    <!--主体内容-->
    <router-view></router-view>
  </div>
</template>

<script>
import Myheader from 'components/Header/Header'
import Mynav from 'components/Nav/Nav'
export default {
  name: 'App',
  components: {
    Myheader,
    Mynav
  },
  data() {
    return {
      poiInfo: {}
    }
  },
  created() {
    var that = this;

    this.$axios.get('/api/goods').then(function(response) {
      // console.log(response);
      var dataSource = response.data;
      if (dataSource.code == 0) {
        that.poiInfo = dataSource.data.poi_info
        // console.log(that.poiInfo);
      }
    }).catch(function(error) {
      console.log(error);
    });
  }
}
</script>

<style>

</style>
