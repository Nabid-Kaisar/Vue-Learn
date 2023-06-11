<script>
  export default {
    props: ['todoLists'],
    emits: ['deleteTodo'],
    methods: {
      handleDelete(idx){
        this.$emit("deleteTodo", idx)
      }
    }
  }
</script>

<template>
  <ol>
    <template v-for="(todo, index) in todoLists" :key="index">
      <div style="display: flex">
        <li style="margin-right: 5px">{{todo}}</li>
        <button @click="()=>handleDelete(index)">Delete Task!</button>
      </div>
    </template>

  </ol>
</template>