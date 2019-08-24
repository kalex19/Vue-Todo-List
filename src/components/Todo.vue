<template>
  <output id="todo" v-bind:class="{'isCompleted': todo.completed}" @click="() => lineThrough()">
    <h3>{{todo.text}}</h3>
  </output>
</template>

<script>

export default {
  name: "Todo",
  props: {
    id: Number,
    text: String,
    completed: Boolean
    },
  methods: {
    lineThrough() { 
      
    }
  }
}
</script>

<style>

.isCompleted {
  text-decoration: line-through;
}


</style>
