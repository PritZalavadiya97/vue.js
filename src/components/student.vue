<template>
    <div>
        <h1>Student</h1>
        <h4>{{mess}}</h4>
        <button v-on:click="get_Message(userName)">Click me</button>
        <br/>
        <input type="text" ref="out" />
        <button v-on:click="myData()">Check it</button>

    </div>
</template>

<script>
export default {
    name : "student",
    props : {
        mess :String,
        get_Message : Function,
    },
    data(){
        return{
            userName : "Student Here.."
        }
    },
    methods:{
        myData(){
            // console.log("Hello");
            this.$refs.out.focus()
            let val = this.$refs.out.value
            console.log(val);
        }
    }
}
</script>

<style scoped>

</style>