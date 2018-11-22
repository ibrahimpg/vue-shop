<template>
  <div class="footerContainer">
    <div>
      <a href="#"><i class="fab fa-instagram fa-2x"></i></a>
      <a href="#"><i class="fab fa-twitter fa-2x"></i></a>
    </div>
    <div>
      <a href="#">Contact</a>
      <a href="#">Returns</a>
      <a href="#">Privacy</a>
      <a href="#">Terms</a>
    </div>
    <div>
      <p>fleXdrip &copy; 2018</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Footer',
};
</script>

<style scoped>
.footerContainer {
  display: flex;
  flex-direction: column;
  background-color: rgba(0,0,0,0.8);
}

.footerContainer > div {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px;
}

.footerContainer > div > a, i, p {
  margin: 0 10px;
  transition: 0.5s;
  text-decoration: none;
  color: white;
}

.footerContainer > div > a:hover, i:hover {
  color: #42b983;
}
</style>
