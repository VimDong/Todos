<!-- HTML -->
<template lang="html">
  <div class="view">
    <h1 class="title">{{ title }}</h1>
    <input v-model="newItem" @keyup.enter="addItem" />
    <ul>
      <li v-for="item in items" :key="item.id" v-bind:class="{finesh:item.isFinished}" @click="toggleFinish(item)">
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
      ],
      newItem: ''
    }
  },
  methods: {
    toggleFinish: function (item) {
      // 改变状态
      item.isFinished = !item.isFinished
    },
    addItem: function () {
      this.items.push({
        text: this.newItem,
        isFinished: false
      })
      this.$emit('fatherFn', this.newItem)
      this.newItem = ''
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
