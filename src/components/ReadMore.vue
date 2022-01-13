<template>
  <p>
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Nostrum iste <span class="dots" v-show="!more">...</span>
    <span class="more" v-show="more"><br/>iusto magni voluptas impedit vitae neque aut eaque repudiandae laboriosam in, minima totam animi sunt aliquam? Architecto at esse labore?</span>
  </p>
<button @click="toggleText()" class="btn-more">{{ buttonText }}</button>
</template>

<script>
export default {
  data(){
    return{
      more: false,
    };
    
  },
  methods:{
    toggleText: function(){
      this.more = !this.more;
    }
  },
  computed: {
    buttonText: function () {
      return this.more ? 'Show Less' : 'Show More';
    }
  }
}
</script>

<style>

</style>