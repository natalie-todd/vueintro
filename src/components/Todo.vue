<template lang='html'>
    <div class=''>
        <form @submit.prevent='addTodo()'>
            <label for='newTodo'>New Todo</label>
            <input v-model='newTodo' type='text' name='newTodo' id='newTodo' value=''>
            <button type='submit' name='button'>Add Todo</button>
            </form>
            <ul>
              <li v-for='todo in todos'>
                {{todo}}
                <button @click='removeTodo(todo)' type='button' name='button'>Remove This Todo</button>
                </li>
            </ul>
            <button @click='clearTodos()' type='button' name='button'>Clear Todos</button>
        </div>
</template>

<script>
export default {
  data() {
    return {
      newTodo: "",
      todos: ['Learn Vue', 'Learn FEFs']
    };
  },
  methods: {
    addTodo() {
      this.todos.push(this.newTodo);
      this.newTodo = "";
    },
    clearTodos() {
      this.todos = [];
    },
    removeTodo(todo) {
      console.log(todo);
      const index = this.todos.indexOf(todo);
      this.todos.splice(index, 1);
    }
  }
};
</script>

<style lang='css'>
</style>
