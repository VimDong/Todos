<template lang="html">
  <div class="headerview">
    <h1>{{title}}</h1>
  </div>
</template>

<script>
export default {
  // props 对象，接受父组件向子组件传参
  props: {
    // 自定义属性
    title: {
      type: String,
      default: '默认标题...'
    }
  }
}
</script>

<style lang="css">
</style>
