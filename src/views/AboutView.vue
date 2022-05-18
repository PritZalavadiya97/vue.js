<template>
  <div class="about">
    <h1>This is an about page</h1>
    <h2 :class="applyStyle">Hello text...</h2>
    <button v-on:click="newColor=!newColor">Apply Style</button>
  </div>
</template>

<script>
export default {
  data(){
    return{
      newColor : false,
      // newColor : true
    }
  },
  computed : {
    applyStyle(){
      return {
          text_color:this.newColor,
          err:true
      }
    }
  }
}
</script>

<style scoped>
.text_color{
  color: red;
}
.err{
  background-color: black;
}
</style>