<template>
  <div id="app">
    <div>{{result}}</div>
  </div>
</template>

<script>
import axios from 'axios'
import {request} from './network/request'
export default {
  name: 'app',
  components: {
    
  },
  data(){
    return{
      result:''
    }
  },
  created () {
    // axios({
    //   url:'http://123.207.32.32:8000/home/multidata'
    // }).then(res=>{
    //   this.result=res;
    // })
    request({
  // url:'/home/multidata'
  url:'/home/data/aaa',
    params:{
      type:'sell',
      page:3
    }
}).then(res=>{
  // console.log(res);
  this.result=res
}).catch(err=>{
  console.log(err); 
})
  }
}
</script>

<style>

</style>
