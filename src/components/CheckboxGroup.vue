<script setup lang="ts">
import { defineProps } from 'vue';

// Define the type for the prop data
interface Item {
  id: number
  label: string
  checked: boolean
}
const props = defineProps<{data: Item[] }>()
</script>

<template>
    <div class="card">
        <div v-for="item in props.data" :key="item.id" >
            <input type="checkbox" :id="item.id" v-model="item.checked" />
            <label>{{ item.label }}</label>
        </div>
    </div>
</template>