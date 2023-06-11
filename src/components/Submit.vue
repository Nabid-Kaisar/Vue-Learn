<script>
  export default {
    props: ["inp"],
    emits: ["addTodo"],
    methods: {
      handleSubmit(){
        this.$emit('addTodo')
      }
    }
  }
</script>

<template>
  <button @click="handleSubmit">Add</button>
</template>