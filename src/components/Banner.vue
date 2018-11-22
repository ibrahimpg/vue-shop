<template>
  <div class="bannerContainer">
    <p>{{msg}}</p>
  </div>
</template>

<script>
export default {
  name: 'Banner',
  props: {
    msg: String,
  },
};
</script>

<style scoped>
.bannerContainer {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: white;
  padding: 3px;
}

p {
  color: rgba(0,0,0,0.8);
}
</style>
