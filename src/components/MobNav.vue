<template>
  <div class="navContainer">
    <div>
      <h4 @click="goHome()">fleXdrip</h4>
      <div v-if="popupMenu" style="display: inline;">
        <i @click="popupMenu = !popupMenu" class="fas fa-times"></i>
      </div>
      <div v-if="!popupMenu" style="display: inline;">
        <i @click="popupMenu = !popupMenu" class="fas fa-bars"></i>
      </div>
    </div>
    <div v-if="popupMenu" style="display: flex; justify-content: center; align-items: center; padding-top: 15px;">
      <router-link to="/shop">Shop</router-link>
      <router-link to="/brand">Brand</router-link>
      <router-link to="/account">Account</router-link>
      <router-link to="/cart"><i class="fas fa-shopping-cart"></i></router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MobNav',
  data(){
    return {
      popupMenu: false,
    }
  },
  watch:{
    $route (to, from){
      this.popupMenu = false;
    }
  },
  methods:{
    goHome(){
      this.$router.push('/')
    }
  } 
};
</script>

<style scoped>
h4 {
  display: inline;
  font-family: 'Cinzel Decorative', cursive;
  margin-right: 10px;
  letter-spacing: 5px;
  cursor: pointer;
}

i { cursor: pointer; }

.navContainer {
  position: sticky;
  top: 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px;
  background-color: #42b983;
  display: none;
}

.navContainer a {
  color: #2c3e50;
  font-weight: bold;
  text-decoration: none;
  border-bottom: 2px solid transparent;
  margin: 0 10px;
  padding: 0 10px;
}

.navContainer a.router-link-exact-active {
  border-bottom: 2px solid #2c3e50;
}

@media only screen and (max-width: 600px) {
  .navContainer {
    display: block;
  }
}
</style>
