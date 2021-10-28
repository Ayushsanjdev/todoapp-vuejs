<template>
  <div>
    <ul class="todos">
      <li class="todo-list" v-for="(todo, index) in todos" :key="index">
        {{ todo }}
        <button class="del-btn" :key="index">X</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  components: {},
  props: ["allTodos"],
  data() {
    return {
      todos: this.allTodos,
    };
  },
  methods: {},
};
</script>

<style scoped>
.todo-list {
  display: flex;
  justify-content: space-between;
  position: relative;
  list-style: none;
  height: 45px;
  line-height: 45px;
  margin-bottom: 8px;
  background: rgb(231, 231, 231);
  border-radius: 3px;
  padding: 0 15px;
}
.todos {
  max-width: 380px;
  margin: 1rem auto;
}
.del-btn {
  border: transparent;
  padding: 0.4rem;
  cursor: pointer;
  height: min-content;
  align-self: center;
  font-weight: bolder;
}
.del-btn:hover {
  background-color: red;
}
</style>