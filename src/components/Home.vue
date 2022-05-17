<template>
    <div>
        <h1>Hello Home.js : {{ 5 + 3 }}</h1>
        <h1>Length : {{"Hello".length}}</h1>
        <h1>Email : {{email}}</h1>
        <h1>Name : {{myName()}}</h1>
        <h2>Get Name : {{getName("Your Name")}}</h2>
        <h2>Here Your Name : {{getYourName()}}</h2>
        <h2>All Data : {{getData().email}}</h2>
        <h2>All Data : {{getData().name}}</h2>
    </div>    
</template>

<script>
export default{
    name : 'Hello',
    data(){
        return {
            email : 'a@gmail.com',
            myName: function(){
                return "Hello Function"
            },
            getName: function(a){
                return a
            }
        }
    },
    methods:{      
        getYourName() 
        {
            return "Get Your Name..";
        },  
        getData()
        {
            return {
                name : "peter",
                email : this.email
            }
        }
    }
}
</script>

<style scoped>

</style>