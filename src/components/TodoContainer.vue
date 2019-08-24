<template>
  <output id="todoContainer">
    <div v-bind:key="todo.id" v-for="todo in todos">
      <Todo v-bind="todo"/>
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
