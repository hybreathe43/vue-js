<script setup>
import { ref } from 'vue';
const name="three hai ya ";
const num = ref(0);
// function say(e){
// console.log(e)
// }

</script>

<template>
  <h1>{{num}}</h1>
  <!-- <button @click="num++">click</button> -->
  <button @click="say">click</button>
  <!-- <button @click="say($event)">click</button> -->
  <div>
    
<h1>HelloWorld {{ name }}</h1>

  </div>

</template>

<style scoped>
</style>
