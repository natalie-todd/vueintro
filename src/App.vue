<template>
  <div id='app'>
    <Todo />
    <!-- <Movies /> -->
    <!-- <h1>{{msg}}</h1>
    <p v-if='isAwesome'>Galvanize is awesome</p>
    <p v-else>Galvanize is NOT awesome</p>
    <ul>
      <li v-for='item in items' :key='item'>{{item}}</li>
    </ul>
    <p :class='{ hideMe: isHidden }'>This is hidden</p> -->
  </div>
</template>

<script>
import Movies from './components/Movies.vue';
import Todo from './components/Todo.vue';

export default {
  name: 'App',
  components: {
    Todo
  },
  data() {
    return {
      msg: 'Hello Galvanize',
      isAwesome: true,
      items: ['Hello World', 'Hello Vue', 'Hello You'],
      isHidden: true,
    };
  },
};
</script>

<style>
.hideMe {
  display: none;
}
</style>
