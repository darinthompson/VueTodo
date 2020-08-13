<template>
    <div id="todo" v-bind:class="{'is-complete':todo.completed}">
        <p>
            <input type="checkbox" v-on:change="markComplete">
            {{ todo.title }}
            <button @click="$emit('del-todo', todo.id)" class="btn alert-danger">Delete</button>
        </p>
    </div>
</template>

<script>
export default {
    name: 'TodoItem',
    props: ["todo"],
    methods: {
        markComplete() {
            this.todo.completed = !this.todo.completed;
        },
        deleteTodo() {
            console.log("I am deleted");
        }
    }
}
</script>

<style scoped>

    .btn {
        margin-left: 5px;
    }
    
    .is-complete {
        text-decoration: line-through;
        color: tomato;
    }
</style>