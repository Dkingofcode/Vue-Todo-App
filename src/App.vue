<script setup lang="ts">
//import Todoform from "./components/TodoForm/TodoForm.vue";
//import TodoListItem from "./components/TodoListItem";


 
</script>



<template>
  <div id="app">
    <h1>TODO</h1>
     <Todoform @onNewTodo="handleNewTodo" />

     <div>
      <TodoListItem v-for="todo in todoList" :key="todo.id" :todo="todo" />
     </div>
  </div>

</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>



