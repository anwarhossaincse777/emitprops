<script setup>

import {ref, reactive} from 'vue'

import Person from './components/Person.vue'
import SingleItem from "./components/SingleItem.vue";
import MultipleItem from "./components/MultipleItem.vue";
import SingleItemUseAsChild from "./components/SingleItemUseAsChild.vue";
import ButtonItem from "./components/ButtonItem.vue";

const person = reactive({
  name: 'John Doe',
  age: 30,
  occupation: 'Web Developer',
})

</script>

<template>
<!--  passing full objec as a props in person-->
<Person :person="person"/>


<!-- how  we pass single object in a component  here the example -->

  <SingleItem v-model="person.name" label="Name" />

  <!-- how  we pass single object in a component  here the another way example -->

  <MultipleItem v-model:name="person.name" v-model:age="person.age" v-model:occupation="person.occupation"/>

<!--  how can child props use in a child-->

<!--  <SingleItemUseAsChild :person="person"/>-->

  <ButtonItem v-model:name="person.name" label="Name"/>

</template>

<style scoped>

</style>
