<template>
    <form id="form" action="submit">
    <label for="todo" class="todoLabel">Today I Have To...</label>
    <input type="text" placeholder="type your todo here" name="todo" class="todoInput">
    <input type="submit" value="Vue Todo" class="submitBtn"/>
    </form>
</template>

<script>


export default {
  data() {
    return {
      todo: ''
    }
  }
}
</script>

<style>

#form {
  margin: 5%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
  width: 50%;
}

.todoLabel {
  font-size: 1.5em;
  font-family: 'Beth Ellen';
}

.todoInput {
  height: 40px;
  width: 300px;
  outline: none;
  font-size: 1.5em;
  background-color: transparent;
  border-color: transparent;
  border-bottom: 2px solid pink;
  font-family: 'Beth Ellen';
  padding-left: 10px;
}

.submitBtn {
  height: 40px;
  width: 100px;
  outline: none;
  font-size: 1.5em;
  background-color: pink;
  font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
}
</style>