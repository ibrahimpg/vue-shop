<template>
  <div>

    <Splash />

    <BrandBand />

    <SecondSplash />

    <div class="container">
      <div class="containerContent">
        <div class="sweaters">
          <router-link to="/shop">Shop</router-link>
        </div>
        <div class="shirts">
          <router-link to="/shop">Shop</router-link>
        </div>
        <div class="accessories">
          <router-link to="/shop">Shop</router-link>
        </div>
        <div class="shoes">
          <router-link to="/shop">Shop</router-link>
        </div>
      </div>
    </div>

    <Email />

  </div>
</template>

<script>
import Splash from '@/components/Splash.vue';
import BrandBand from '@/components/BrandBand.vue';
import SecondSplash from '@/components/SecondSplash.vue';
import Email from '@/components/Email.vue';

export default {
  name: 'home',
  components: {
    Splash,
    BrandBand,
    SecondSplash,
    Email,
  },
};
</script>

<style scoped>
.shirts {
  background: url(../assets/shirts.jpg) no-repeat center; background-size: cover;
}

.sweaters {
  background: url(../assets/sweaters.jpg) no-repeat center; background-size: cover;
}

.accessories {
  background: url(../assets/accessories.jpg) no-repeat center; background-size: cover;
}

.shoes {
  background: url(../assets/shoes.jpg) no-repeat center; background-size: cover;
}

.container {
  display: flex;
  justify-content: center;
  align-items: center;
}

.containerContent {
  width: 800px;
  margin: 10px 0;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
}

.containerContent > div {
  width: 350px;
  height: 350px;
  margin: 10px;
  display: flex;
  align-items: flex-start;
  box-shadow: 0 4px 6px 0 hsla(0, 0%, 0%, 0.2);
}

.containerContent > div > a {
  text-decoration: none;
  color: white;
  margin: 10px;
  border-radius: 15px 5px 15px 5px;
  background-color: rgba(0,0,0,0.8);
  padding: 5px 30px;
}
</style>
