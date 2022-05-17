<template>
    <div>
        <h1>
            {{data.name}}
            {{data.email}}
            <button v-on:click="getData(data.name)">Model Click</button>
        </h1>
    </div>
</template>

<script>
export default {
    name : "user",
    props: {
        data : Object,
        getData : Function,
    }
}
</script>