<script setup>
const message = 'Hello Vue!'
const isActive = false
</script>
<template>
    <div>
        <p>訊息: {{message}}</p>
        <p>計算: {{1+1}}</p>
        <p>呼叫方法: {{message.toUpperCase()}}</p>
        <p>三元運算: {{ isActive ? "啟用": "停用"}}</p>
    </div>
</template>
<style scoped></style>