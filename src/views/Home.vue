<template>
  <div class="home">
    <div class="flex">
      <div class="icon">
        <van-cell @click="showPopup">
          <van-icon name="wap-nav" />
        </van-cell>
        <van-popup
          v-model="show"
          round
          position="left"
          :style="{ width: '70%',height:'100%'}"
        >
          <sidebar />
        </van-popup>
      </div>
      <div class="title">云音乐</div>
      <div class="icon">
        <router-link to="/search">
        </router-link>
      </div>
    </div>
    <div class="wrap">
      <van-row>
        <router-link
          to="/sheet"
          tag="div"
        >
          <van-col>推荐</van-col>
        </router-link>
        <router-link
          to="/ranking"
          tag="div"
        >
          <van-col>歌单</van-col>
        </router-link>
        <router-link
          to="/singer"
          tag="div"
        >
          <van-col>歌手</van-col>
        </router-link>
      </van-row>
    </div>
    <div class="cover">
      <keep-alive>
        <router-view></router-view>
      </keep-alive>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  }
}
</script>
<style scoped>
.flex {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: rgb(42, 41, 48);
}
.icon .van-cell {
  background: rgb(42, 41, 48);
}
.icon i {
  font-size: 2rem;
  cursor: pointer;
}
.title {
  font-weight: 600;
  color: #ffffff;
}
.wrap {
  width: 100%;
  background: rgb(42, 41, 48);
  font-size: 0.8rem;
  height: 2rem;
}
.van-row {
  width: 100%;
  display: flex;
  justify-content: space-around;
  color: #ffffff;
}
.van-row div {
  margin-left: 1.5rem;
}

.cover {
  height: 100vh;
  width: 100%;
  margin-top: 3rem;
}
</style>