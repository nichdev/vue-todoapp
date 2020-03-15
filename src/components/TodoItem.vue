<template>
    <div class='todo-item-box'>
        <div>
            <button class="todo-item" v-bind:class="{'is-completed':todo.completed}" v-on:click="markComplete">{{ todo.title }}</button>
        </div>
        <button @click="$emit('del-todo', todo.id)" class='unit del'><i class="material-icons">
delete_outline
</i></button>
    </div>
</template>

<script>
export default {
    name: "TodoItem",
    props: ["todo"],
    methods: {
        markComplete() {
            this.todo.completed = !this.todo.completed;
        }
    },
}
</script>


<style scoped>
    .todo-item-box {
        padding: 10px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .is-completed {
        text-decoration: line-through;
    }

    .del {
        border-radius: 8px;
        color: #AE1100;
    }
</style>