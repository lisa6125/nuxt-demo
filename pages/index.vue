<template>
  <div class="container">
    <p>我是首頁</p>
    <p>照片輪播</p>
    <img :src="res[pic].url" alt="">
    <button @click="change(-1)">上一張</button>
    <button @click="change(1)">下一張</button>
  </div>

</template>

<script>
import axios from 'axios';
export default {
  name:'index',
  layout:'default',
  async asyncData(){
    const res = await axios.get('https://vue-lessons-api.herokuapp.com/photo/list')
    return {res:res.data};
  },
  data(){
    return {
      res:[],
      pic:0,
    }
  },
  methods:{
    change(num){
      if(this.pic + num === -1){
        this.pic = this.res.length-1
      }else{
        this.pic = (this.pic + num ) % this.res.length
      }
    }
  }
}
</script>

<style>

</style>