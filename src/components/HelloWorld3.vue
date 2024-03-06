<script setup>
import {inject} from "vue";
const name="three hai ya";
const ing=inject("name");
const desc=inject("desc","not available");
</script>

<template>
  <div>
<h1>HelloWorld {{ name }}{{ ing }}{{ desc }}</h1>

<!-- <slot name="header"></slot>
<slot name="footer"></slot>
<slot name="mid"></slot> -->
<!-- <slot nm="saasssshil" :age="23"></slot> -->
  </div>

</template>

<style scoped>
</style>
