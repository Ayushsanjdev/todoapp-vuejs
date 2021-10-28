<template>
  <div class="input-area">
    <input placeholder="Enter Todo" v-model="newTodo" class="input-box" />
    <button class="add-btn" @click="addTodo">Add</button>
  </div>
</template>

<script>
export default {
  props: ["allTodos"],
  data() {
    return {
      newTodo: null,
      todos: this.allTodos,
    };
  },
  methods: {
    addTodo() {
      this.todos.push(this.newTodo);
      this.newTodo = '';
    },
  },
};
</script>

<style scoped>
.input-area {
  display: flex;
  justify-content: center;
  gap: 1rem;
}
.input-box {
  border: 2px groove grey;
  padding: 0.7rem;
  width: 300px;
}
.add-btn {
  padding: 0 1rem;
}
</style>