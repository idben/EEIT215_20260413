<script setup>
import { ref, reactive } from 'vue'

const fruits = ref([
    { id: 1, name: '蘋果' },
    { id: 2, name: '香蕉' },
    { id: 3, name: '橘子' },
])

const profile = reactive({
    姓名: '小明',
    年齡: 25,
    信箱: 'ming@example.com',
    城市: '台北'
});

const newFruit = ref('');

const addFruit = () => {
    if (!newFruit.value) return;
    console.log(newFruit.value);
    const obj = {
        id: Date.now(),
        name: newFruit.value
    }
    console.log(obj);
    fruits.value.push(obj);
    newFruit.value = "";
}
</script>
<template>
    <div>
        <ul>
            <li v-for="(fruit, index) in fruits" :key="fruit.id">
                {{ index + 1 }}. {{ fruit.name }}
                <button @click="fruits.splice(index, 1)">刪除</button>
            </li>
        </ul>
        <input type="text" v-model="newFruit" @keyup.enter="addFruit">
        <h1>個人資料</h1>
        <div v-for="(value, key) in profile" :key="key">
            {{ key }}: {{ value }}
        </div>
    </div>
</template>
<style scoped></style>