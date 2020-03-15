<template>
    <header class="header">
        <h1>Todo List</h1>
        <div id="nav">
            <router-link to="/">
                <button>Home</button>
            </router-link>
            <router-link to="/about">
                <button>About</button>
            </router-link>
        </div>
    </header>
</template>

<script>
export default {
    name: "Header"
}
</script>

<style lang="stylus" scoped>
    .header{
        padding-top 50px;
        padding-bottom 30px
        color: #fff;
        text-align: center;

        a {
            color: #fff;
            padding-right: 5px;
            text-decoration: none;
        }

        h1 {
            color: #BABECC;
            text-shadow: 1px 1px 1px #fff;
            margin-bottom 24px;
        }
    }

    #nav {
        button {
            margin 0 6px;
            border-radius 8px
        }
    }
</style>