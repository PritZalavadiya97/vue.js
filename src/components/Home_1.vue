<template>
    <div>
        <h1>Home_1 component</h1>
        <button v-on:click="test()">Click Me</button>
        <button v-on:click="getData()">Click Me + </button>
        <button v-on:click="get_Data()">Click Me - </button>
        <button v-on:dblclick="getData('Button 2 Click')">Click Me</button>
        <h2 v-on:mousemove="move()">Mouse Hover</h2>
        <h3>{{count}}</h3>
        <student mess="student props" :get_Message="getMessage"/>
        <h1>{{childData}}</h1>
    </div>    
</template>

<script>

import student from "../components/student.vue"

export default{
    name : "Home_1",
    data(){
        return{
            count :0,
            childData : ""
        }
    },
    methods : {
        test() {
            alert("Hello test");
        },
        getData() {
            this.count = this.count + 1;
        },
        get_Data() {
            this.count = this.count - 1;
        },
        getMessage(userName){
            this.childData = userName
        }
    },
    components : {
        student,
    }
}
</script>

<style scoped>

</style>