<script setup lang="ts">
import { ref } from 'vue'
import ReturnContentType from './ReturnContentType.vue';

const input = ref("")

const submitText = () => {
    console.log(input.value)
}
</script>

<template>
    <label>What skill would you like to learn?</label>

    <div class="card">
        <input type="text" v-model="input" class="input-box" />
        <ReturnContentType />
        <button type="submit" @click="submitText" class="submit-button">Generate</button>
    </div>
</template>

<style scoped>
.card {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}
.input-box{
    width: 80%;
    height: 2rem;
}
.submit-button {
    width: 50%;
    height: 3rem;
    margin-top: 10px;
}
</style>
