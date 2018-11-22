<template>
  <div>

    <div class="container pc">
      <div>
        <b>Eco-Friendly</b><br>
        <p>Made 100% out of recycled cotton and polyester.</p>
      </div>
      <div>
        <b>Wage Hope</b><br>
        <p>50% of profits go to <a href="#">Charity Name</a>.</p>
      </div>
      <div>
        <b>Look Fresh</b><br>
        <p>Some other gibberish about something.</p>
      </div>
    </div>

    <div class="container mobile">

      <i @click="slideLeft()" class="fas fa-arrow-circle-left fa-3x"></i>

      <div v-if="slideCount === 1">
        <b>Eco-Friendly</b><br>
        <p>Made 100% out of recycled cotton and polyester.</p>
      </div>
      <div v-if="slideCount === 2">
        <b>Wage Hope</b><br>
        <p>50% of profits go to <a href="#">Charity Name</a>.</p>
      </div>
      <div v-if="slideCount === 3">
        <b>Look Fresh</b><br>
        <p>Some other gibberish about something.</p>
      </div>

      <i @click="slideRight()" class="fas fa-arrow-circle-right fa-3x"></i>

    </div>

  </div>
</template>

<script>
export default {
  name: 'BrandBand',
  data() {
    return {
      slideCount: 1,
    };
  },
  methods: {
    slideLeft() {
      if (this.slideCount === 1) {
        this.slideCount += 2;
      } else {
        this.slideCount -= 1;
      }
    },
    slideRight() {
      if (this.slideCount === 3) {
        this.slideCount -= 2;
      } else {
        this.slideCount += 1;
      }
    },
  },
};
</script>

<style scoped>

i { cursor: pointer; }
i, p, b { color: rgba(0,0,0,0.8); }

.pc { display: flex; }
.mobile { display: none; }

@media only screen and (max-width: 800px) {
  .mobile { display: flex; }
  .pc { display: none; }
}

.container {
  justify-content: space-evenly;
  align-items: center;
  padding: 50px 0;
}

.container > div {
  width: 200px;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
}
</style>
