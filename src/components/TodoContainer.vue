<template>
  <output id="todoContainer">
    <div v-bind:key="todo.id" v-for="todo in todos">
      <Todo v-bind="todo" v-on:del-todo="$emit('del-todo', todo.id)"/>
    </div>
  </output>
</template>

<script>
import Todo from "./Todo.vue"

export default {
  name: "TodoContainer",
  components: {
    Todo
  },
  props:["todos"]
}
</script>

<style>

</style>
