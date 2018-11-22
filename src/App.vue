<template>
  <div id="app">
    <Nav />
    <MobNav />
    <Banner msg="FREE SHIPPING ON ORDERS ABOVE $30" />
    <router-view/>
    <Footer />
  </div>
</template>

<script>
import Nav from '@/components/Nav.vue';
import MobNav from '@/components/MobNav.vue';
import Banner from '@/components/Banner.vue';
import Footer from '@/components/Footer.vue';

export default {
  components: {
    Nav,
    MobNav,
    Footer,
    Banner,
  }
}
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  font-family: 'Kanit', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
