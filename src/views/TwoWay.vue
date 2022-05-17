<template>
  <div class="contact">
    <h1>This is an Two Way page</h1>

    <input type="text" v-model="count">
    <h2>{{count}}</h2>


    <br/>
    <input type="text" placeholder="entry name" v-model="name">
    <br/>
    <input type="text" placeholder="entry email" v-model="email">

    <button v-on:click="getData()">Get Values</button>

    <br/><br/>
    <label for="java">java</label>
    <input type="checkbox" value="java" id="java" v-model="technology">
    <label for="js">js</label>
    <input type="checkbox" value="js" id="js" v-model="technology">
    Technology : <h4>{{technology}}</h4>
    <br/><br/>

    <h3>Who I am</h3>
    <label for="student">Student</label>
    <input type="radio" value="student" id="student" name="radio_btn" v-model="who">

    <label for="developer">Developer</label>
    <input type="radio" value="developer" id="developer" name="radio_btn" v-model="who">
    Who I am : <h4>{{who}}</h4>


    <h4 v-if="show">If Condtion</h4>
    <h4 v-else>Else Condtion</h4>
    <button v-on:click="show=!show">Toggle</button>

    <h1>For Loop in Vue JS</h1>
    
    <p v-for="index of new_array" :key="index">
        {{index}}
    </p>

    <p v-for="item of user" :key="item">
        {{item.age}} |
        {{item.email}}
    </p>

    <child massage= "hello child" :new_array_="new_array_" :newData="newData"/>

  </div>
</template>

<script>

import child from '../components/Child.vue'

export default {
    data(){
        return {
            count : 10,
            name:null,
            email:null,
            technology : [],
            who : null,
            show : true,
            new_array : ["abc","bcd","cdf"],
            user : [
                {
                    name:"abc",
                    email:"a@gmail.com",
                    age:20
                },
                {
                    name:"bcd",
                    email:"b@gmail.com",
                    age:54
                },
                {
                    name:"cdf",
                    email:"c@gmail.com",
                    age:44
                }
            ],
            new_array_ : {
                name:"abc",
                email:"a@gmail.com"
            }
        }
    },
    methods : {
        getData(){
                console.log(this.email, this.name);
        },
        newData(){
            console.log("New Data");
        }
    },
    components : {
        child,
    }
}
</script>

