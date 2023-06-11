<script>
  import UserInput from "./UserInput.vue"
  import Submit from "./Submit.vue"
  import TodoList from "./TodoList.vue"

  export default {
    data(){
      return {
        todoLists: ['learn vue pt 1', 'write some code', 'Do some testing'],
        inp: ''
      }
    },
    methods: {
      handleAddTodo(){
        this.todoLists.push(this.inp);
        this.inp = "";
      },
      handleDeleteTodo(idx){
        this.todoLists.splice(idx, 1);
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
  <UserInput @addTodo="handleAddTodo" @onChange="(val)=> this.inp = val" :inp="inp"/>
  <TodoList @deleteTodo="(idx) => handleDeleteTodo(idx)" :todoLists="todoLists"/>
  <Submit @addTodo="handleAddTodo" :inp="inp"/>
</template>