<template>
  <div class="todo">
    <h1>{{ title }}</h1>
    <h3>{{ subtitle }}</h3>
    <list />
  </div>
</template>

<script>
  import List from './List.vue'

  export default {
    data () {
      return {
        title: 'Vue Todo App!',
        subtitle: 'Add some items below!'
      }
    },
    components: {List}
  }
</script>

<style scoped>
  h1, h2 {
    color: #42b983;
  }
</style>
