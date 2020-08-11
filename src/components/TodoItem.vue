<template>
    <div id="todo" v-bind:class="{'is-complete':todo.completed}">
        <p>
            <input type="checkbox" v-on:change="markComplete">
            {{ todo.title }}
            <button @click="$emit('del-todo', todo.id)" class="btn">Delete</button>
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
    .is-complete {
        text-decoration: line-through;
        color: tomato;
    }
</style>