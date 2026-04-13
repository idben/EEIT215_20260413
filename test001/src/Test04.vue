<script setup>
import {ref} from 'vue'

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
    </div>
</template>
<style scoped>
img{
    width: 200px;
}
a{
    display: block;
}
.circle{
    width: 50px;
    height: 50px;
    border-radius: 50%;
    background-color: #edb9b9;
}
</style>