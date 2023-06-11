<script>
  import TodoApp from "./components/TodoApp.vue"
  import Header from "./components/Header.vue"
  export default {
    components: {
      TodoApp,
      Header
    }
  }
</script>

<template>
  <Header />
  <TodoApp />
</template>