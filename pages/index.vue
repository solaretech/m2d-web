<template>
  <div>
    <AddToDo @submit="addToDo"  />
    <TodoList :todos="todos" />
  </div>
</template>

<script>
import AddToDo from '@/components/AddTodo'
import TodoList from '@/components/TodoList'

export default {
  components: {
    AddToDo,
    TodoList
  },
  data () {
    return {
      todos: []
    }
  },
  methods: {
    addToDo (title) {
      this.todos.push({
        title
      })
    }
  }
}
</script>

<style>
</style>
