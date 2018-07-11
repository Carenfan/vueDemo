<template>
 <section class="jumbotron">
   <h3 class="jumbotron-heading">search Github Users</h3>
   <div>
     <input type="text" placeholder="enter the name you search" v-model="searchName">
     <button @click="search">search</button>
   </div>
 </section>
</template>

<script>
  //引入消息接收
 import Pubsub from 'pubsub-js'
   export default {  //配置对象
      data (){
        return{
          searchName:""
        }
      },
     methods:{   //发布消息前先得到消息
        search(){
          const searchName = this.searchName.trim()
          if(searchName){
            //发布消息（search）
            Pubsub.pubslish("search",searchName)
            this.searchName=''
          }
        }
     }
}
</script>

<style scoped>

</style>
