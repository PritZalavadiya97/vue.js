<template>
  <div class="contact">
      <h2>Simple Form</h2>
     
      <form @submit.prevent>
        <div>
          <label>First Name</label>
          <input type="text" v-model="from.name">
        </div>
        <div>
          <label>Email</label>
          <input type="text" v-model="from.email">
        </div>
        <div>
          <label>Password</label>
          <input type="password" v-model="from.password">
        </div>
        <div>
          <select v-model="from.country">
            <option>Abc</option>
            <option>Bca</option>
            <option>Cab</option>
          </select>
        </div>
        <div>
          <h3>Technology</h3>
          <label>Yes Technology</label>
          <input type="checkbox" v-model="from.technology" value="yes">
          
          <label>No Technology</label>
          <input type="checkbox" v-model="from.technology" value="no">
        </div>
        
        <div>
          <h3>Gender</h3>
          <label>Male</label>
          <input type="radio" v-model="from.gender" value="male" name="gender_name">
          
          <label>Famale</label>
          <input type="radio" v-model="from.gender" value="famale" name="gender_name">
        </div>
        <button type="submit" v-on:click="login">Submit</button>
      </form>
      <ul>
        <li v-for="item_error of error" :key="item_error">
          {{item_error}} not valid
        </li>
      </ul>
  </div>
</template>

<script>



export default {
  data(){
    return{
      from: {
        name : '',
        email : '',
        password : '',
        country : '',
        technology : [],
        gender : '',
      },
      error: [],
    }
  },
  methods :{
    login(){
      this.error = [];
      for (const item in this.from){
          if(this.from[item] === "" || this.from[item].length === 0){
            this.error.push(item)
          }
      }

      // if(this.error.length === 0){
      //   alert("Data Submited")
      // }

      console.log("login Data", this.from);
    }
  }
   
}
</script>

