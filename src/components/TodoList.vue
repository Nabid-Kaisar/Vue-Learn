<script>
  export default {
    props: ['todoLists'],

    created() {
      console.log(this.todoLists);
    }
  }
</script>

<template>
  <ol>
    <li v-for="(todo, index) in todoLists" :key="index">{{todo}}</li>
  </ol>
</template>