<script setup lang="ts">
import { ref } from 'vue'

// Define an array of items for the checkboxes
const items = ref([
    { id: 1, label: 'Videos', checked: false },
    { id: 2, label: 'Written Materials', checked: false },
    { id: 3, label: 'Nearby Organizations', checked: false },
])

const levels = ref([
    { id: 1, label: 'Beginner', checked: false },
    { id: 2, label: 'Intermediate', checked: false },
    { id: 3, label: 'Expert', checked: false },
])

</script>

<template>
    <div class="card">
        <div v-for="item in items" :key="item.id" class="checkbox-group">
            <input type="checkbox" :id="item.id" v-model="item.checked" />
            <label>{{ item.label }}</label>
        </div>
        <div v-for="level in levels" :key="level.id" class="">
            <input type="checkbox" :id="level.id" v-model="level.checked" />
            <label>{{ level.label }}</label>
        </div>
    </div>
</template>

<style scoped>
.card {
    background-color: grey;
}
</style>
