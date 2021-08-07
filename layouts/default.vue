<template>
  <div>
    <Header />
    <nuxt-link to="/">首頁</nuxt-link>
    <nuxt-link to="/about">about</nuxt-link>
      <p>------這邊是layout，裡面是router-view-----</p>
      <Nuxt />
      <p>---------------------------------------</p>
    <Footer />
  </div>
</template>

<script>
export default {

}
</script>

<style>

</style>