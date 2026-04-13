<script setup>
import { ref } from 'vue';

const score = ref(75);

</script>
<template>
    <div>
        <h1>分數: {{ score }} <span v-show="score == 100">⭐</span></h1>
        <div v-if="score >= 90">優等</div>
        <div v-else-if="score >= 70">甲等</div>
        <div v-else-if="score >= 60">乙等</div>
        <div v-else>不及格</div>
        <input type="number" v-model.number="score">
    </div>
</template>
<style scoped></style>