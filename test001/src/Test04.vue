<script setup>
import { ref } from 'vue'

const imageUrl = 'https://images.pexels.com/photos/16197273/pexels-photo-16197273.jpeg'
const link = 'https://images.pexels.com/photos/16197273/pexels-photo-16197273.jpeg'
const className = "circle"
const isLoading = ref(true)
const textColor = "pink"
const textSize = 36;

</script>
<template>
    <div>
        <img :src="imageUrl" alt="">
        <a :href="link">點擊我</a>
        <div :class="className"></div>
        <button :disabled="!isLoading">點擊我</button>
        <button class="btn" :class="{ disable: !isLoading }">點擊我(物件式)</button>
        <button :class="['btn', { disable: !isLoading }]">點擊我(陣列式)</button>
        <div :style="{ color: textColor, fontSize: textSize + 'px' }">綁定 style</div>
    </div>
</template>
<style scoped>
img {
    width: 200px;
}

a {
    display: block;
}

.circle {
    width: 50px;
    height: 50px;
    border-radius: 50%;
    background-color: #edb9b9;
}

.btn {
    padding: 4px;
    padding-left: 8px;
    padding-right: 8px;
    width: fit-content;
    background-color: #01aaff;
    border-radius: 5px;
    color: #fff;
    user-select: none;
    cursor: pointer;

    &:hover {
        background-color: #006eff;
    }

    &.disable {
        background-color: #646464;
        cursor: not-allowed;
    }
}
</style>