<template>
  <div class="secondSplashContainer">
    <h3>50% OFF BLACK FRIDAY SALE</h3>
  </div>
</template>

<script>
export default {
  name: 'SecondSplash',
}
</script>

<style scoped>
h3 {
  color: white;
  background-color: rgba(0,0,0,0.8);
  padding: 10px;
}

.secondSplashContainer {
  display: flex;
  height: 500px;
  justify-content: flex-end;
  align-items: center;
  background: url(../assets/sale.jpg) no-repeat center; background-size: cover;
}
</style>
