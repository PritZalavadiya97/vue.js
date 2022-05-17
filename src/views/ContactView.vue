<template>
  <div class="contact">
    <h1>This is an contact page</h1>
    <p v-for="index of myData" :key="index">
      <user :data="index" :getData="getData"/>
      <!-- {{index.name}} -->
    </p>
  </div>
</template>

<script>

import user from "../components/User.vue";

export default {
  data(){
    return{
      myData : [
        {
          name : "abc",
          email : "a@gmail.com"
        },
        {
          name : "bca",
          email : "b@gmail.com"
        },
        {
          name : "cab",
          email : "c@gmail.com"
        }
      ]
    }
  },
  components :{
    user,
  },
  methods :{
    getData(name){
      alert(name)
    }
  }
}
</script>
