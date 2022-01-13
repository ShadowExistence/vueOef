<template>
  <VisibleInput msg="Welcome to My Vue.js App"/>
  <ShoppingList />
  <ReadMore />
  <TipCalculator />
  <ImageChanger />
</template>

<script>
import VisibleInput from './components/VisibleInput.vue'
import ShoppingList from './components/ShopingList.vue'
import ReadMore from './components/ReadMore.vue'
import TipCalculator from './components/TipCalculator.vue'
import ImageChanger from './components/ImageChanger.vue'

export default {
  name: 'App',
  components: {
    VisibleInput,
    ShoppingList,
    ReadMore,
    TipCalculator,
    ImageChanger
  }, 
}
</script>

<style>
div{
  margin-bottom: 50px;
  text-align: center;
}
</style>