<template>
  <div class="todo"  >
    <input  v-bind:class="{'isCompleted':completed}" :value="text"/>
    <button @click="$emit('line-through')" class="checkBtn">✔️</button>
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
  display: grid;
  grid-template-columns: 75% 12.5% 12.5%;
  justify-content: space-evenly;
  text-align: left;
  width: 30%;
}

h3 {
  font-size: 2em;
  outline: none;
}

.isCompleted {
  text-decoration: line-through;
  text-decoration-color: pink;
}

.deleteBtn,
.checkBtn {
  border-radius: 50%;
  height: 30px;
  width: 30px;
  font-size: .5em;
  outline: none;
}


</style>
