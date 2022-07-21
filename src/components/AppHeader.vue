<script setup>
  defineProps(['color'])
</script>

<template>
  <header>
    <h1 v-bind:style="{ 'color': color}"><slot>Default Title</slot></h1>
  </header>
</template>