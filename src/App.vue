<template>
  <div>
    <h1 class="head">Todo App</h1>
    <AddTodo :allTodos="allTodos" />
    <Todos :allTodos="allTodos" />
  </div>
</template>

<script>
import AddTodo from "./components/addTodo.vue";
import Todos from "./components/todos.vue";

export default {
  name: "App",
  components: {
    AddTodo,
    Todos,
  },
  data() {
    return {
      allTodos: ["first todo", "second totdos"],
    };
  },
};
</script>

<style scoped>
.head {
  text-align: center;
  padding: 2rem 0;
}
</style>
