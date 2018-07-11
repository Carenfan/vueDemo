<template>
  <div class="todo-container">
    <div class="todo-wrap">
      <todo-header :addTodo="addTodo"/>
      <List :todos="todos" :deleteTodo="deleteTodo"/>
      <todo-footer :todos="todos" :deleteComputed="deleteComputed" :selectAll="selectAll"/>
    </div>
  </div>
</template>

<script>    //scoped :范围内
 import Header from './components/Header.vue'
 import List from './components/List.vue'
 import Footer from './components/Footer.vue'


export default {  //配置对象
  data(){
    return{
      todos:[
        {title:'eat',completed:false},
        {title:'sleep',completed:ture},
        {title:'knock code',completed:false},

      ]
    }

  },
  components:{
    todoHeader:Header ,
    List,
    TodoFooter:Footer
  },

}
</script>

<style>

</style>
