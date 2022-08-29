<script setup>
// eslint-disable-next-line no-undef,no-unused-vars
const props = defineProps({
  todo: Object
})
</script>

<template>
  <li>{{ todo.text }}</li>
</template>