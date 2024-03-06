<script setup>
import {computed,inject,onMounted,onBeforeMount} from "vue";
const ing=inject("name");
const desc=inject("desc","not available");
const props=defineProps({modelValue:String});
const emit =defineEmits(["update:modelValue"]);

const value=computed({
    get(){
        return props.modelValue;
    },
    set(value){
        emit("update:modelValue",value);
    }
})

</script>
<template>
    <h1>{{ ing }}{{ desc }}</h1>
     <input type="text" :style="{color:'red'}" :value="modelValue" @input="$emit('update:modelValue',$event.target.value)">
    <input type="text" :style="{color:'red'}" v-model="value">
    </template>
<style scoped></style>