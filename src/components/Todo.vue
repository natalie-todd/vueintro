<template lang='html'>
    <div class=''>
        <form @submit.prevent='addTodo()'>
            <label for='newTodo'>New Todo</label>
            <input type='text' name='newTodo' id='newTodo' value=''>
            <button type='submit' name='button'>Add Todo</button>
            </form>
            <ul>
              <li v-for='todo in todos'>{{todo}}</li>
            </ul>
        </div>
</template>

<script>
export default {
  data() {
    return {
      newTodo: '',
      todos: [],
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

<style lang='css'>
</style>
