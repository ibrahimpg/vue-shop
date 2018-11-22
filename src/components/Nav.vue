<template>
  <div class="navContainer">

    <div>
      <h4>fleXdrip</h4>
      <router-link to="/">Home</router-link>
      <router-link to="/shop">Shop</router-link>
      <router-link to="/brand">Brand</router-link>
    </div>

    <div>
      <router-link to="/account">Account</router-link>
      <router-link to="/cart"><i class="fas fa-shopping-cart"></i></router-link>
    </div>

  </div>
</template>

<script>
export default {
  name: 'Nav',
};
</script>

<style scoped>
h4 {
  display: inline;
  font-family: 'Cinzel Decorative', cursive;
  margin-right: 10px;
  letter-spacing: 5px;
}

.navContainer {
  position: sticky;
  top: 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
  background-color: #42b983;
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
    display: none;
  }
}
</style>
