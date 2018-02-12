<!-- HTML -->
<template lang="html">
  <div class="view">
    <h1 class="title">{{ title }}</h1>
    <ul>
      <li v-for="item in items" :key="item.id" v-bind:class="{finesh:item.isFinished}">
      {{item.text}}
      </li>
    </ul>
  </div>
</template>

<!-- JavaScript -->
<script>
// 类似于 new Vue()
export default {
  name: 'List',
  data () {
    return {
      title: 'Todos',
      items: [
        {
          text: '今天晚上 18:00 跑步',
          isFinished: false
        },
        {
          text: '今晚吃水果晚餐',
          isFinished: true
        }
      ]
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
  .view .title {
    border-bottom: 1px solid gray;
  }
  .view ul li {
    margin: 10px 0;
    list-style: none;
  }
  .view .finesh {
    color: gray;
    text-decoration: line-through;
  }
</style>
