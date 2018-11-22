<template>
  <div class="splash">
    <div class="sticker">
      <h2>NEW COLLECTION</h2>
      <h2>Shop Now</h2>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Splash',
}
</script>

<style scoped>
.splash {
  height: 100vh;
  background-color: gray;
  background: #fff url('../assets/flex.jpg') no-repeat top;
  background-size: cover;
  background-attachment: fixed;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
}

.sticker {
  background:linear-gradient(to right, #42b983, #42b983 90%, green 90%, green 95%, orange 95%);
  padding: 10px 50px 10px 10px;
}
</style>
