<script setup lang="ts">
//import Todoform from "./components/TodoForm/TodoForm.vue";
//import TodoListItem from "./components/TodoListItem";
 
import { ref, computed, onMounted, watch } from "vue";
import TodoForm from './components/TodoForm/TodoForm.vue';
import TodoListItem from './components/TodoListItem/TodoListItem.vue';

const todoList = [
  //  { text: "bring food" },
  //  { text: "save money" },
]

const name = ref('');

const input_content = ref('');
const input_category = ref(null);

const todos_asc = computed(() => todos.value.sort((a, b) => {
  return a.createdAt - b.createdAt
}))
</script>



<template>

<div id="app">
    <h1 className="heading">TODO</h1>
    <div>
     <TodoForm @onNewTodo="handleNewTodo" />
     </div>  

     <div>
      <TodoListItem v-for="todo in todoList" :key="todo.id" :todo="todo" />
     </div>
  </div>

</template>

<style scoped>

*{
  margin: 0;
  padding: 0;
  border: 0;
  box-sizing: border-box;
}

#app{
  border: 5px solid;
  margin: 0 auto;
  margin-left: 90px;
  display: flex;
  height: 300px;
  justify-content: center;
  width: 200px;
  flex-direction: column;
  align-items: center;
}

.heading{
  text-align: center;
}



</style>



