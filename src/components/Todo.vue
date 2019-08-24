<template>
  <div class="todo" v-bind:class="{'isCompleted':completed}">
    <h3 @click="$emit('line-through')">{{text}}</h3>
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
    }
}
</script>

<style>

.todo {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  width: 30%;
}

h3 {
  font-size: 2em;
}

.isCompleted {
  text-decoration: line-through;
  text-decoration-color: pink;
}

.deleteBtn {
  border-radius: 50%;
  height: 30px;
  width: 30px;
  font-size: .5em;
  outline: none;
}


</style>
