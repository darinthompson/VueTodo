<template>
  <div class="library">
    <h1>Here are all the books!</h1>
    <Books v-bind:books="books" />
  </div>
</template>

<script>
import Books from "../components/Books.vue";
export default {
  name: "Library",
  components: {
    Books
  },
  data() {
    return {
      books: [
        {
          id: 1,
          title: "Streams of Silver",
          author: "R.A. Salvatore",
        },
        {
          id: 2,
          title: "Deep Fathom",
          author: "James Rollins",
        },
        {
            id: 3,
            title: "Bible",
            author: "Various"
        }
      ]
    };
  },
};
</script>

<style scoped>

</style>