<template>
  <div id="app">
    <div class="container">
      <div class="row">
        <app-card 
          :cardWords="card" 
          :msg="msg" 
          @resetMyCar="onClickChangeCard()"
          :changeMsg="onClickChangeMsg"
        ></app-card>
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
        card: 'BMW',
        msg: 'This is my car !'
     
      }
    },
    methods: {
      onClickChangeCard(){
        this.card = 'Suzuki'
      },
      onClickChangeMsg(){
        this.msg = 'This is your car !'
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
