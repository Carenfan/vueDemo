<template>
  <div  >
   <search/>
   <user-main/>
  </div>
</template>

<script>
  //引入组件
import Search from './components/Search.vue'
import Main from './components/Main.vue'

  export default {  //配置对象
    components:{
        Search,
        UserMain:Main
    }


  }
</script>

<style scoped >
  .jumbotron {
    width: 600px;
    margin: 0 auto;
  }
   .jumbotron-heading {
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 5px;
  }
</style>
