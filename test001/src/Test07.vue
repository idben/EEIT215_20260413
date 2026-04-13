<script setup>
import { ref } from 'vue';

const userID = ref("ben")
const userPWD = ref("")

const handleSubmit = (e) => {
    // e.preventDefault();
    // console.log({ userID, userPWD }); // 簡寫, 但要屬性和來源一模一樣才能簡寫
    console.log({ userID: userID.value, userPWD: userPWD.value });
}

</script>
<template>
    <form @submit.prevent>
        <div class="row">
            <label for="userID">ID</label>
            <input type="text" name="userID" id="userID" placeholder="輸入使用者帳號" v-model="userID"
                @keydown.shift.enter.prevent="handleSubmit">
        </div>

        <div class="row">
            <label for="userPWD">password</label>
            <input type="password" name="userPWD" id="userPWD" placeholder="輸入密碼" v-model="userPWD"
                @keydown.shift.enter.prevent="handleSubmit">
        </div>

        <div class="ctrl">
            <button @click="handleSubmit">送出</button>
        </div>

    </form>
</template>
<style scoped>
.row {
    display: flex;

    input {
        flex: 1;
    }
}

.ctrl {
    display: flex;
    justify-content: flex-end;
}
</style>