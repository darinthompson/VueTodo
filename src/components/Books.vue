<template>
    <div id="books">
        <div v-for="book in books" v-bind:key="book.id">
            <book v-bind:book="book" />
        </div>
    </div>
</template>

<script>
import Book from './Book.vue';
export default {
    name: 'Books',
    components: {
        Book
    },
    props: ['books']
}
</script>

<style scoped>

</style>