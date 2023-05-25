<template>
  <div id="app">
    <div class="container">
      <div class="row">
        <app-card :cardWords="card" @resetMyCar="onClickChangeCard()"></app-card>
      </div>
    </div>
  </div>
</template>

<script>
  import Card from './components/Card.vue'

  export default {
    components: {
      'app-card': Card
    },
    data() {
      return {
        card: 'BMW'
      }
    },
    methods: {
      onClickChangeCard(){
        this.card = 'Suzuki'
      }
    },
    

  }
</script>

<style>
  body {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

</style>
