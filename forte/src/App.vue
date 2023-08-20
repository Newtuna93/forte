<template>
  <div>
    <img alt="Vue logo" src="./assets/logo.png">
    <!--<HelloWorld msg="Welcome to Your Vue.js App 신동원입니다."/>-->
    <kakaoMap />
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import kakaoMap from './kakao/kakaoMap.vue'

export default {
  name: 'App',
  data() {
    return {};
  },
  components: {
    kakaoMap,
  },
  methods: {

  },
  mounted() {
    // 페이지가 렌더링 된 이후! (created 이후에 동작한다고 함)
    // alert("say Hello!");
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
