<script setup>
defineProps(['modelValue','label'])
defineEmits(['update:modelValue'])
</script>


<template>


  <p class="my-5">
    <h2 class="text-xl">Child from singleItem</h2>
  </p>


  {{ modelValue}}

  <p>
    <form class="flex flex-col">
      <label for="name">{{label}}</label>
      <input type="text" id="name" name="name" :value="modelValue" @input="$emit('update:modelValue',$event.target.value)">
    </form>
  </p>


</template>


<style scoped>

</style>