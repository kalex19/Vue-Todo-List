<template>
  <div class="todo" v-bind:class="{'isCompleted':completed}">
    <h3 @click="lineThrough">{{text}}</h3>
    <button @click="$emit('del-todo')" class="deleteBtn">X</button>
  </div>
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
      this.completed = !this.completed;
    }
  }
}
</script>

<style>

.todo {

}

h3 {
  font-size: 3em;
}

.isCompleted {
  text-decoration: line-through;
  text-decoration-color: pink;
}

.deleteBtn {
  border-radius: 50%;
  height: 50px;
  width: 50px;
  font-size: 1.5em;
  outline: none;
}


</style>
