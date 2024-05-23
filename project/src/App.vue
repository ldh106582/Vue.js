<template>
  <div id="app">
      <h1 class="text-center">Todo App</h1>
      <input v-model="todoText" type="text" class="p-2" @keyup.enter="addTodo" placeholder="what?">
      <hr>
    <TodoItem v-for="todo in todos" :key="todo.id" :todo="todo"/>
  </div>
</template>

<script>
import TodoItem from '@/components/Todo.vue';

export default 
{
  components: {
    TodoItem
  },
  data()
  {
    return {
      todoText: '',
      todos: [
        { id: 1, text: 'buy a car', checked: false },
        { id: 2, text: 'play a car', checked: false },
      ]
    }
  },
  methods: 
  {
    addTodo(e)
    {
      this.todos.push ({
        id: Math.random(),
        text: e.target.value,
        checked: false
      });
      this.todoText = '';
    }
  }
}

</script>


<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
