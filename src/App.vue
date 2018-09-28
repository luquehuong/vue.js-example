<template>
  <div>
    <todo-list v-bind:todos="todos"></todo-list>
    <create-todo v-on:create-todo="createTodo"></create-todo>
  </div>
</template>


<script>
import TodoList from "./components/TodoList";
import CreateTodo from "./components/CreateTodo";

export default {
  name: "app",
  components: {
    TodoList,
    CreateTodo
  },
  // data function avails data to the templete
  data() {
    return {
      todos: [
        {
          title: "Todo A",
          project: "Project A",
          done: false
        },
        {
          title: "Todo B",
          project: "Project B",
          done: false
        },
        {
          title: "Todo C",
          project: "Project C",
          done: false
        }
      ]
    };
  },
  methods: {
    createTodo(newTodo) {
      this.todos.push(newTodo);
    }
  }
};
</script>
