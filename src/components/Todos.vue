<template>
    <div class='todo-box'>
       <div v-for="(todo, index) in todos" :key="index">
           <TodoItem v-bind:todo="todo" v-on:del-todo="$emit('del-todo', todo.id)"/>
       </div>
    </div>
</template>

<script>
import TodoItem from './TodoItem';
export default {
    components: {
        TodoItem
    },
    name: "Todos",
    props: ["todos"]
}
</script>

<style lang="stylus" scoped>
    .todo-box {
        margin-top: 30px;
    }
</style>