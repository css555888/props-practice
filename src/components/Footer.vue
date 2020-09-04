<template>
    <footer>
        <p>{{copylight}}</p>
    </footer>
</template>

<script>
export default {
    name: 'app-footer',
    data(){
        return {
            copylight:"copylight 2020 vue demo"
        }
    }
}
</script>

<style scoped>
    footer{
        background: #222;
        padding: 10px;
    }
    p{
        color: lightgreen;
        text-align: center;
    }
</style>