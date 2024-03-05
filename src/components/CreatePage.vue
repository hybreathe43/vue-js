<template>
<div>
    
  <label for="fname">Page title</label><br>
  <input type="text" v-model="v1"  ><br>
  <label for="lname">Content</label><br>
  <input type="text" v-model="v2"><br><br>
  <button @click.prevent="pageCreated" :disabled="computedValue">Submit</button>

</div>

</template>
<script setup>
import { ref,computed  } from "vue";
let v1 = ref(" ");
let v2 = ref(" ");
function pageCreated(){
    if(!v1){
  alert("FILL FORM",v1);
        return;
    }

    alert("dddd"+v1.value+" "+v2.value);
    // localStorage.setItem("name", v1);
}
const computedValue = computed(() => {
  return !v1.value
});
// export default{
//     props:['pageCreated']
// }
</script>