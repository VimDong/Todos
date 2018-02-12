<template>
  <div id="app">
    <headerview :title="title"></headerview>
    <img src="./assets/logo.png">
    <listview @fatherFn="getDate"></listview>
  </div>
</template>

<script>
import listview from './components/List'
import headerview from './components/Header'

export default {
  name: 'App',
  components: {
    listview,
    headerview
  },
  data () {
    return {
      title: 'Vue 入门学习'
    }
  },
  methods: {
    getDate (msg) {
      console.log('新添加的 ITEM：' + msg)
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
