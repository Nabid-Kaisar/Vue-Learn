<script>
  export default {
    props: ["inp"],
    methods: {
      handleSubmit(){
        console.log(this.inp)
      }
    }
  }
</script>

<template>
  <button @click="handleSubmit">Add</button>
</template>