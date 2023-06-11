<script>
  export default {
    props: ["inp"],
    emits: ["onChange", "addTodo"],
    methods: {
      handleChange(e){
        this.$emit('onChange', e.target.value)
      },
      handleKeyDown(e){
        if(e.key === 'Enter'){
          this.$emit('addTodo')
        }
      }
    }
  }
</script>
<template>
  <input @keydown="handleKeyDown" :value="inp" @change="handleChange" />
</template>