<script setup>
import SingleItem from "../App.vue";
defineProps(['person'])

</script>

<template>
  <h1>I am form singleItem used</h1>
  <SingleItem v-model="person.name" label="Name"/>
</template>

<style scoped>

</style>