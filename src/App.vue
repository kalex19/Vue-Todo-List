<template>
  <div id="app">
    <Header/>
    <Form />
    <TodoContainer v-bind:todos="todos" v-bind:loading="loading"/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Form from './components/Form.vue'
import TodoContainer from './components/TodoContainer.vue'

export default {
  name: 'app',
  components: {
    Header,
    Form,
    TodoContainer
  }, 
  data() {
    return {
      todos: [
        {
          id: 1,
          text: "Todo One",
          completed: false
        },
        {
          id: 2,
          text: "Todo Two",
          completed: false
        },
        {
          id: 3,
          text: "Todo Three",
          completed: false
        }
      ],
      loading: false
    }
  }
}
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  }

body {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-image: url('./assets/lauren-sauder-6GPBVYLapYQ-unsplash.jpg');
  background-repeat: no-repeat;
}
</style>
