<template>
  <div class="container">
    <p>我是首頁</p>
    <p>我的名字是 {{ name }} </p>
    <button @click="change()">改名字</button>
  </div>

</template>

<script>
export default {
  name:'index',
  layout:'default',
  asyncData(){
    const name = 'mike';
    return {name};
  },
  data(){
    return {
      name:'',
    }
  },
  methods:{
    change(){
      this.name = 'tom不是mike'
    }
  }
}
</script>

<style>

</style>