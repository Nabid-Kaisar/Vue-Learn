<script>
  export default {
    emits: ["onChange"],
    methods: {
      handleChange(e){
        this.$emit('onChange', e.target.value)
      }
    }
  }
</script>
<template>
  <input @change="handleChange" />
</template>