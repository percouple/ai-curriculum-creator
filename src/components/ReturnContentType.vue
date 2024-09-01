<script setup lang="ts">
import { ref } from 'vue'

// Define an array of items for the checkboxes
const items = ref([
  { id: 1, label: 'Videos', checked: false },
  { id: 2, label: 'Written Materials', checked: false },
  { id: 3, label: 'Checkbox 3', checked: false },
])
</script>

<template>
    <div class="card">
    <div v-for="item in items" :key="item.id" class="checkbox-group">
      <input
        type="checkbox"
        :id="item.id"
        v-model="item.checked"
      />
      <label :for="item.id">{{ item.label }}</label>
    </div>
  </div>
</template>

<style scoped>
.card {
    background-color: grey;
}
</style>
