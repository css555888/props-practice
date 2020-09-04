<template>
    <div class="users">
        <h1>Hello users</h1>
        <ul>
            <li v-for="user in abc" @click="user.show=!user.show">
                <!-- 注意点：父组件传过来的是abc，而不是users，所以user in users 需要改成user in abc -->
                <h2>{{user.name}}</h2>
                <h3 v-show="user.show">{{user.position}}</h3>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'users',
    // props: ['users'],
    props:{
        abc:{
            type:Array,
            required:true
        }
    },
    data(){
        return {
            
        }
    }
}
</script>

<style scoped>
    .users{
        width: 100%;
        max-width: 1200px;
        margin:  40px auto;
        padding: 0 20px;
        box-sizing: border-box;
    }
    ul{
        display: flex;
        flex-wrap: wrap;
        list-style-type: none;
        padding: 0;
    }
    li{
        flex-grow: 1;
        flex-basis: 200px;
        text-align: center;
        padding: 30px;
        border: 1px solid #222;
        margin: 10px;
    }
</style>