<template>
  <div>
    <input type="text" v-model='inputValue'>
    <button @click='submit'>提交</button>
    <todo-item v-for='(item, index) in lists' :key='index' :content='item' :index='index' @delete='deleteFather'></todo-item>
  </div>
</template>

<script>
  import TodoItem from './components/TodoItem.vue'

  export default {
    data() {
      return {
        inputValue: '',
        lists: []
      }
    },
    methods: {
      submit() {
        this.lists.push(this.inputValue);
      },
      deleteFather(index) {
        this.lists.splice(index, 1);
      }
    },
    components: {
      'todo-item': TodoItem
    }
  }
</script>

<style>
</style>
