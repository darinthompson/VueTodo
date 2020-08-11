<template>
    <div>
        <h1>I am the todos</h1>
        <div v-for="todo in todos" v-bind:key="todo.id">
            <TodoItem class="item" v-bind:todo="todo" v-on:del-todo="$emit('del-todo', todo.id)"/>
        </div>
    </div>
</template>

<script>
import TodoItem from './TodoItem.vue';

export default {
    name: "Todos",
    components: {
        TodoItem
    },
    props: ["todos"]
}
</script>

<style scoped>

</style>
