<template>
    <div>
        <h3>{{ book.title }}</h3>
        <p> {{ book.author }}</p>
    </div>
</template>

<script>
export default {
    name: 'Book',
    props: ['book']
}
</script>

<style scoped>

</style>