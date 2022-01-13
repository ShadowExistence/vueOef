<template>
  <h2>Tip Calculator</h2>
  <p>How much is the total bill?</p>
  <input type="text" id="amount" v-model="price">
  <p>How goed was the service?</p>
  <select name="refer" id="percentage" v-model="percent">
    <option value="30">30% (Exceptional)</option>
    <option value="25">25% (More than good)</option>
    <option value="20" selected>20% (Good)</option>
    <option value="15">15% (It was okay)</option>
    <option value="10">10% (Bad)</option>
    <option value="5">5% (Terrible)</option>
  </select>

  <p>How many people are sharing the bill?</p>
  <input type="text" id='people' v-model="ppl">


  <p>tip emount = {{ calculate }}</p>
</template>

<script>
export default {
  data(){
    return{
      price: "10",
      percent: "",
      ppl : ""
    }
  },
  computed:{
    calculate (){
      return (this.price * this.percent / 100) / this.ppl;
    }
  }
}
</script>

<style>

</style>