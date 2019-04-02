<template>
  <div id="app">
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div> -->
    <Container></Container>
    <Footer></Footer>
  </div>
</template>
<script>
import Container from '@/components/Container.vue';
import Footer from '@/components/Footer.vue';
export default {
  name:'app',
  components:{
    Container,
    Footer
  }
}
</script>

<style lang="scss">

</style>
