<template>
    <div>
        <h1>Home_1 component</h1>
        <button v-on:click="test()">Click Me</button>
        <button v-on:click="getData()">Click Me + </button>
        <button v-on:click="get_Data()">Click Me - </button>
        <button v-on:dblclick="getData('Button 2 Click')">Click Me</button>
        <h2 v-on:mousemove="move()">Mouse Hover</h2>
        <h3>{{count}}</h3>
    </div>    
</template>

<script>
export default{
    name : "Home_1",
    data(){
        return{
            count :0
        }
    },
    methods : {
        test() {
            alert("Hello test");
        },
        getData() {
            this.count = this.count+1;
        },
        get_Data() {
            this.count = this.count-1;
        },
        move(){
            // console.warn("yes warn")
        }
    }
}
</script>

<style scoped>

</style>