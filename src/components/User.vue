<template>
    <div>
        <h1>
            {{data.name}}
            {{data.email}}
            <button v-on:click="getData(data.name)">Model Click</button>
        </h1>

        <h2>{{text}}</h2>
        <div v-html="tag">

        </div>

        <h2 :class="{green:newcolor}">text here...</h2>

      

    </div>
</template>

<script>


export default {
    name : "user",
    props: {
        data : Object,
        getData : Function,
    },
    data(){
        return {
            text : "Hello Text",
            tag : "<b>HTML Tag</b>",
            newcolor : true
        }
    }
}
</script>

<style scoped>
.green{
    color: red;
}
</style>