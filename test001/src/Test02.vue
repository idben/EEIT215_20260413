<script setup>
import { reactive } from 'vue';

const user = reactive({
  name: '小明',
  age: 25,
  email: 'ming@example.com'
})
const items = reactive(['蘋果', '香蕉', '橘子'])
user.name = "小美";
items.unshift("西瓜");
</script>
<template>
    <div>
        <h1>{{user.name}}</h1>
        <h3>{{user.age}}</h3>
        <h4>{{user.email}}</h4>
        <h4>{{items[0]}}</h4>
    </div>

</template>
<style scoped></style>