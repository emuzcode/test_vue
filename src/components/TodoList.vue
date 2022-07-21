<script setup>
defineProps(['todos'])

const emit = defineEmits(['removeTodo'])

const clickRemove = (i) => emit('removeTodo', i)
</script>

<template>
<ul v-if="todos.length > 0">
  <li v-for="(t, i) in todos" v-bind:key="i">{{t}} <span v-on:click="clickRemove(i)" style="cursor: pointer">X</span> </li>
</ul>
<p v-else>*add your to-do</p>
</template>
