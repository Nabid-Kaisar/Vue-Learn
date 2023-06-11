<script>
  export default {
    props: ['todoLists'],
    emits: ['deleteTodo', 'editTodo'],
    methods: {
      handleDelete(idx){
        this.$emit("deleteTodo", idx)
      },
      handleEdit(idx, newValue){
        this.$emit("editTodo", idx, newValue)
      }
    }
  }
</script>

<template>
  <ol>
    <template v-for="(todo, index) in todoLists" :key="index">
      <div style="display: flex">
        <li style="margin-right: 5px">{{todo}}</li>
        <button style="margin-right: 5px" @click="()=>handleDelete(index)">Delete Task!</button>
        <button @click="()=>handleEdit(index, 'editedStatic')">Edit Task!</button>
      </div>
    </template>

  </ol>
</template>