<!-- HTML -->
<template lang="html">
  <div class="view">
    <h1>{{ title }}</h1>
  </div>
</template>

<!-- JavaScript -->
<script>
// 类似于 new Vue()
export default {
  name: 'List',
  data () {
    return {
      title: 'Todos'
    }
  }
}
</script>

<!-- CSS -->
<style lang="css">
  .view {
    width: 400px;
    border: 1px solid gray;
    margin: 20px auto;
  }
</style>
