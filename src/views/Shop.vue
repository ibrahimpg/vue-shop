<template>
  <div>
    <div class="shopNav">
      <p>T-SHIRTS</p>
      <p>SWIM TRUNKS</p>
      <p>ACCESSORIES</p>
    </div>
    <div class="shopContainer">
      <div class="shopContent">
        <div v-for="item in items" :key="item.id">
          {{item.name}} {{item.price}}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {name: 'whatever', price: '32'},
        {name: 'hey', price: '12'},
        {name: 'whatever', price: '32'},
        {name: 'hey', price: '12'},
        {name: 'whatever', price: '32'},
        {name: 'hey', price: '12'},
      ]
    }
  }
}
</script>


<style scoped>

.shopNav {
  display: flex;
  padding: 20px 0 20px 20px;
  background-color: rgba(0,0,0,0.8);
}

.shopNav > p {
  margin: 0 10px;
  color: white;
  cursor: pointer;
  transition: 0.5s;
}

.shopNav > p:hover {
  color: #42b983;
}

.shopContainer {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.shopContent {
  width: 1000px;
  border: 1px solid black;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
}

.shopContent > div {
  width: 300px;
  height: 300px;
  border: 1px solid black;
  margin: 20px 0;
}

</style>
