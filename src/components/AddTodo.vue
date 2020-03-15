{<template>
    <div>
        <form @submit="addTodo">
            <input type="text" v-model="title" name="title" placeholder="Add Todo...">
            <button type="submit" class="unit">+</button>
        </form>
    </div>
</template>

<script>
// import {v4 as uuidv4} from "uuid";
export default {
    name: "AddTodo",
    data() {
        return {
            title: ''
        }
    },
    methods: {
        addTodo(e) {
            e.preventDefault();
            const newTodo = {
                // id: uuidv4(),
                title: this.title,
                completed: false
            }
            // Send up to parent
            this.$emit('add-todo', newTodo);
            this.title = '';
        }
    }
}
</script>

<style lang="stylus" scoped>
    form {
        display: flex;
        padding  10px;
    }
    input[type="text"] {
        flex: 10;
    }
    button[type="submit"] {
        margin-left: 12px;
        width: 16px*3;
        height: 16px*3;
    }
</style>