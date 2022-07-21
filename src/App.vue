<script setup>
import AppHeader from './components/AppHeader.vue'
import {ref} from 'vue'
import TodoList from './components/TodoList.vue';
const todo = ref('')
const todos = ref([])

const addTodo = () => {
  todos.value.push(todo.value)
  todo.value = ''
} 

const removeTodo = (index) => {
  todos.value.splice(index, 1)
}

</script>

<template>
<AppHeader color="blue">My Todo -Slot-</AppHeader>
<input type="text" size="30" v-model="todo">
<button v-on:click="addTodo()">add</button>
<TodoList v-bind:todos="todos" @removeTodo="removeTodo" />
</template>