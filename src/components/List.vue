<template>
  <div class='list'>
    <ul>
      <li v-for='todo in todos'>
        <span class='col-xs-10 todo-title'>{{ todo.title }}</span>
        <button class='col-xs-2 btn btn-danger' v-on:click='removeItem($index)'>X</button>
      </li>
    </ul>
    <input label='Item' v-model='newTodo'>
    <button class='btn btn-default' v-on:click='addItem'>Add Item</button>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        todos: [],
        newTodo: ''
      }
    },
    methods: {
      addItem () {
        const todo = this.newTodo.trim()
        if (todo) {
          this.todos.push({ title: todo })
          this.newTodo = ''
        }
      },
      removeItem (index) {
        this.todos.splice(index, 1)
      }
    }
  }
</script>

<style scoped>
  li {
    list-style: none
  }

  .todo-title {
    font-size: 3rem;
  }
</style>
