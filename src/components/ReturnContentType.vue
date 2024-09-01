<script setup lang="ts">
import { ref } from 'vue'

import CheckboxGroup from './CheckboxGroup.vue'

// Define an array of items for the checkboxes
const items = ref([
    { id: 1, label: 'Videos', checked: false },
    { id: 2, label: 'Written Resources', checked: false },
    { id: 3, label: 'Nearby Organizations', checked: false },
    { id: 4, label: 'Nearby Experts', checked: false},
    { id: 5, label: 'Starting Materials', checked: false},

])

const levels = ref([
    { id: 1, label: 'Beginner', checked: false },
    { id: 2, label: 'Intermediate', checked: false },
    { id: 3, label: 'Expert', checked: false },
])

</script>

<template>
    <div class="card">
        <CheckboxGroup :data="items" class="checkbox-group"/>
        <CheckboxGroup :data="levels" class="checkbox-group" />
    </div>
</template>

<style scoped>
.card {
    background-color: grey;
}
</style>
