<template>
  <section id="todoContainer">
    <div v-bind:key="todo.id" v-for="todo in todos">
      <Todo v-bind="todo" v-on:del-todo="$emit('del-todo', todo.id)" v-on:line-through="$emit('line-through', todo.id)"/>
    </div>
  </section>
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

#todoContainer {
  margin: 15% 30%;
  width: 60%;
  transform: rotate(345deg);
}

</style>
