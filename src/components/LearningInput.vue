<script setup lang="ts">
import { ref } from 'vue'

const input = ref("")
</script>

<template>
    <label>What skill would you like to learn?</label>

    <div class="card">
        <input type="text" v-model="input" class="input-box" />
        <button type="button" @click="" class="submit-button">Generate</button>
    </div>
</template>

<style scoped>
.card {
    display: flex;
    justify-content: center;
}
.input-box{
    width: 100%;
}
.submit-button {
    width: 100%;
}
</style>
