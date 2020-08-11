<template>
    <div>
       <form @submit="addTodo">
           <input type="text" v-model="title" name="title" placeholder="Add Todo...">
           <input type="submit" value="Submit" class="btn">
       </form>
    </div>
</template>

<script>
import {v4 as uuidv4} from "uuid";


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
                id: uuidv4(),
                title: this.title,
                completed: false
            }

            this.$emit('add-todo', newTodo);
            this.title = '';
        }
    }
}
</script>

<style scoped>
    .btn {
        background-color: #666;
        color: white;
        padding: 7px;
    }

    .btn:hover {
        background-color: dimgrey;
    }
</style>