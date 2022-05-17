<template>
<div>
    <h2>Child Componet</h2>
    <h1> {{massage}} </h1>
    <h1> {{new_array_.name}} </h1>
    <h1> {{new_array_.email}} </h1>
    <button v-on:click="newData()">Child Click</button>
</div>
</template>
<script>
export default{
    name : 'child',
    props : {
        massage : String,
        new_array_ : Object,
        newData : Function
    }
}
</script>
