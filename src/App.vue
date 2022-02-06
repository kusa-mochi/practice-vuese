<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld :msg="testMessage">
    <template v-slot:header>
      <div>へっだー</div>
    </template>
    <div>ぼでぃ</div>
  </HelloWorld>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  data() {
    return {
      testMessage: "めっせーじてすてす"
    };
  },
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
