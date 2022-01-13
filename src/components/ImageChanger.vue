<template>
  <img :src="images[cm]" width="100" height="125">
  <button @click="prev()">Previous</button>
  <button @click="next()">Next</button>
</template>

<script>
export default {
  data(){
    return{
       images: [
                 'https://i.imgur.com/rmydi2w.jpg', 
                 'https://i.imgur.com/rAFqZiM.jpg', 
                 'https://i.imgur.com/Fpw5KKY.jpg', 
                 'https://i.imgur.com/IbYRmoW.jpg', 
                 'https://i.imgur.com/9poVrgA.jpg'
                 ],
        cm : 0
    }
  },
  methods:{

    prev(){
      if(this.cm == 0){
        this.cm = 4
        return
      }
      this.cm = this.cm - 1; 
    },
    next(){
      if(this.cm == 4){
        this.cm = 0;
        return
      }
      this.cm = this.cm + 1;
    }
  }
}
</script>
  
<style>

</style>