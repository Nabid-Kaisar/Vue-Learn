<script>
  import UserInput from "./UserInput.vue"
  import Submit from "./Submit.vue"
  import TodoList from "./TodoList.vue"

  export default {
    data(){
      return {
        todoLists: ['learn vue pt 1', 'write some code', 'Do some testing']
      }
    },
    components:{
      UserInput,
      Submit,
      TodoList,
    }
  }
</script>

<template>
  <UserInput />
  <TodoList :todoLists="todoLists"/>
  <Submit />
</template>