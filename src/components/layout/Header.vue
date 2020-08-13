<template>
    <header class="header">
        <h1>TodoList</h1>
        <div id="nav">
            <router-link to="/">Home</router-link> |
            <router-link to="/about">About</router-link> |
            <router-link to="/Library">Books</router-link>
        </div>
    </header>
</template>

<script>
export default {
    name: 'Header'
}
</script>

<style scoped>
    header {
        color: tomato;
        background-color: #333;
    }
    h1 {
        padding-top: 15px;
        margin: 0 auto;
    }

    .header {
        padding-bottom: 20px;
    }
    
    .header a {
        color: #fff;
        text-decoration: none;
        padding-bottom: 10px;
    }
    
</style>