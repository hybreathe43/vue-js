<script setup>

import HelloWorld3 from './HelloWorld3.vue';
import { ref } from 'vue';
// const props =defineProps(["name"])
const props =defineProps({
  name:String,
  age:Number
})

// const name="three hai ya ";
const num = ref(0);
function say(e){
console.log(e)
}

</script>

<template>
  <h1>Hell worlds</h1>
  <HelloWorld3/>
  <!-- <h1>{{num}}</h1> -->
  <!-- <button @click="num++">click</button> -->
  <!-- <button @click="say">click</button> -->
  <!-- <button @click="say($event)">click</button> -->
  <div>
    <!-- <button @click="$emit('increamentNum')" >inc</button> -->
<!-- <h1>HelloWorld {{ name }} age : {{ age }}</h1> -->

  </div>

</template>

<style scoped>
</style>
