<script setup>
import { ref,computed,reactive,provide,onMounted,
onBeforeMount,onUpdated,onBeforeUnmount,onBeforeUpdate,onUnmounted  } from "vue";
import CreatePage from './components/CreatePage.vue';
import HelloWorlds from './components/HelloWorlds.vue';
import HelloWorld3 from './components/HelloWorld3.vue';
import InputCustom from './components/InputCustom.vue';

onMounted(()=>{
    console.log("mounted");
})
onBeforeMount(()=>{
    console.log("before");
})
provide("name"," injection key data");
provide("desc"," injection key desc");

const url="www.google.com";
const obj={
  id:"jack",
  href:"www.google.com"
}
const styleObj=reactive({
  color:"red",
  background:"green"
})
const fon=reactive({
  fontSize:"40px"
})

let fName=ref("sahil mubeen bhi");
let lname=ref("mubeen bhi");
let count=ref(0);
let nnn=ref("");
// import HelloWorld from './components/HelloWorld.vue'
// import TheWelcome from './components/TheWelcome.vue'
let name=" sahil";

const prntName=()=>{
  return fName.value + name + " mubeen";
}
// setTimeout(() => {
//   fName.value="sahil just",
//   name=" sahil also"
// }, 2000);

// const lastName=computed({
//   get(){
//     return lname.value + "sss";
//   },
//   set(neww){
//     console.log(neww);
//     lname.value = neww + " aaaa"
//   }
// })

// setTimeout(() => {
//   lastName.value="sahil"
// }, 2000);
const stu =ref(['sahil',"mubeen","azeem bi"]);
function incby(){
  count.value++;
}
</script>

<template>
  <h1>first</h1>
  <HelloWorlds/>
  <!-- <HelloWorld3>
    <h1>sahil slot</h1>
  </HelloWorld3> -->
  <!-- <HelloWorld3 v-slot="slotProps">
    <h1>sahil slot {{ slotProps.nm }}{{ slotProps.age }}</h1>
  </HelloWorld3> -->
  <!-- <HelloWorld3>
  <template v-slot:header><h1>sahil slot</h1></template>
  <template v-slot:mid><h3>sahil slot</h3></template>
  <template v-slot:footer><h6>sahil slot</h6></template>
  </HelloWorld3>
  <HelloWorld3>
  <template #header><h1>sahil slot</h1></template>
  <template #mid><h3>sahil slot</h3></template>
  <template #footer><h6>sahil slot</h6></template>
  </HelloWorld3> -->
  
  <!-- <h1 v-for="(s,i) in stu" :key="i">{{s}}</h1> -->
  <!-- <h1 v-for="n in 5" :key="n">{{n}}</h1> -->
  <div>
    
    <!-- <InputCustom v-model="nnn" /> -->
    <!-- <InputCustom v-model:first-name="nnn" /> use firstName instead of modelValue in inputcustom  -->
    <h1 v-show="false" >hello</h1>
    <!--  {{prntName() }}<br/>
    {{lastName}} -->
<h1 :id="name" :style="{color:'red',backgroundColor:'pink'}">HelloWorld {{ name }}</h1>
<h1 :id="name" :class="{head}" >HelloWorld {{ name }}</h1>
<a :href="url" :style="[styleObj,fon]" :class="{head}">visit</a><br/>
<a v-bind="obj">visit</a>
<h1>{{ count }}</h1>
<HelloWorlds @increamentNum="incby" />
<!-- <HelloWorlds @increamentNum="count++" /> -->
<!-- <HelloWorlds @increament-num="count++" /> -->

<!-- <HelloWorlds name="ik ik ik" :age="23" /> -->
<!-- <HelloWorlds :name="lname" /> -->
<CreatePage/>
  </div>
  <header>
    <!-- <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" /> -->

    <!-- <div class="wrapper">
      <HelloWorld msg="You did it!" />
    </div> -->
  </header>

  <main>
    <!-- <TheWelcome /> -->
  </main>
</template>

<style scoped>
.head {
  background-color:red;
  }
/* header {
  line-height: 1.5;
}


.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }


  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
} */
</style>
