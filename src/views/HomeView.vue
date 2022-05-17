<template>
  <div class="home">
    <img alt="Vue logo" src="@/assets/logo.png">
    <!-- <HelloWorld message="Welcome to Your Vue.js Project."/> -->
    <HelloWorld message= 120 get_message = "Hello..."/>
    <Hello/>
    <HomeOne/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import Hello from '../components/Home.vue'
import HomeOne from '../components/Home_1.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld,
    Hello,
    HomeOne
  }
}
</script>
