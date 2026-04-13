<script setup>
import { ref } from 'vue';

const count = ref(0);
let count2 =  ref(0);
const msg = ref("HelloWorld Vue");
const name = ref('Vue');
const isVisible = ref(true);
const items = ref(['蘋果', '香蕉', '橘子']);

count.value = 1;
count.value++;
items.value[count.value] = "西瓜"
</script>
<template>
    <h1>{{msg}}</h1>
    <h2>{{count}}</h2>
    <h1>{{name}}</h1>
    <h3>{{isVisible}}</h3>
    <h1>{{ items[count] }}</h1>
    <h1>{{count2}}</h1>
    <button v-on:click="count2++">點擊我</button>
</template>
<style scoped>
h1{
    font-weight: bold;
    text-align: center;
}
</style>