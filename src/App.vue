<template>
<!-- 模板 -->
  <div id="app">
    <app-header></app-header>
    <users v-bind:abc="users"></users>
    <app-footer></app-footer>
  </div>
</template>


<script>
  import Header from './components/Header'
  import User from './components/User'
  import Footer from './components/Footer'

  export default {
    name: 'app',
    data(){
        return {
            users:[
                {name:"helun",position:"web 开发",show:false},
                {name:"helun",position:"web 开发",show:false},
                {name:"helun",position:"web 开发",show:false},
                {name:"helun",position:"web 开发",show:false},
                {name:"helun",position:"web 开发",show:false},
                {name:"helun",position:"web 开发",show:false},
                {name:"helun",position:"web 开发",show:false},
                ]
        }
    },
    components:{
      "app-header":Header,
      "users":User,
      "app-footer":Footer
    }
}
</script>

<style>
</style>
